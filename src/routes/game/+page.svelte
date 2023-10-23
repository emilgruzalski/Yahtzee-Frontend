<script lang="ts">
	let you = 1;

	enum PlayerState {
		THINKING_SELECTION,
		CONFIRMED_SELECTION
	}
	interface PlayerData {
		username: string;
		state: PlayerState;
		dices: Dice[];
	}
	interface Dice {
		value: number;
		selected: boolean;
	}

	let stakes = [5, 10, 25];
	let playerAData = {
		username: 'matbmp',
		state: PlayerState.THINKING_SELECTION,
		dices: [6, 6, 6, 6, 6].map((x) => ({ value: x, selected: false }))
	};
	let playerBData = {
		username: 'emilio',
		state: PlayerState.CONFIRMED_SELECTION,
		dices: [1, 2, 3, 4, 5].map((x) => ({ value: x, selected: false }))
	};
	let players: (PlayerData | null)[] = [null, playerAData, playerBData, null];

    function stakeChosen(stakeIndex: number) {
        
    }

	function confirmSelection() {
		if (players[you] != null) {
			players[you]!.state = PlayerState.CONFIRMED_SELECTION;
		}
	}
</script>

<div class="h-full grid grid-cols-2 grid-rows-2">
	{#each players as player, index}
		<div class="border-2 p-2">
			{#if player}
				<div class="font-bold">{player.username}</div>
				<div class="flex items-center gap-2">
					<div>Current dices:</div>
					{#each player.dices as dice}
						<button
							class="px-4 py-2 rounded-md {dice.selected ? 'bg-amber-200' : 'bg-gray-200'}"
							on:click={() => {
								if (you == index && player && player.state == PlayerState.THINKING_SELECTION) {
									dice.selected = !dice.selected;
								}
							}}
						>
							{dice.value}
						</button>
					{/each}
					{#if player.state == PlayerState.CONFIRMED_SELECTION}
						<span class="text-green-700 font-bold">Action commited</span>
					{/if}
				</div>

				{#if you == index}
					<button class="btn-primary-full" on:click={confirmSelection}>Confirm</button>
				{/if}

				{#if you == index}
                <div class="flex items-center gap-2">
					<div>Choose stake:</div>
					{#each stakes as stake, index}
						<button class="px-4 py-2 rounded-md bg-gray-200" on:click={() => stakeChosen(index)}>
							{stake}
						</button>
					{/each}
                </div>
				{/if}
			{/if}
		</div>
	{/each}
</div>
