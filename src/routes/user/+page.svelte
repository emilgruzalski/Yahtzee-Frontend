<script lang="ts">
	interface UserData {
		username: string;
		email: string;
		coins: number;
	}
	let user: UserData = {
		username: 'matbmp',
		email: 'matbmp@gmail.com',
		coins: 100000000
	};

	let isEditingUsername: boolean = false;
	let isEditingEmail: boolean = false;

	function startEditUsername() {
		isEditingUsername = true;
	}

	function endEditUsername() {
		isEditingUsername = false;
	}

	function startEditEmail() {
		isEditingEmail = true;
	}

	function endEditEmail() {
		isEditingEmail = false;
	}
</script>

<div class="h-full flex items-center justify-center">
	<div
		class="flex flex-col items-center p-4 mx-4 w-full xl:w-1/2 h-5/6 rounded-lg border border-gray-400 bg-gray-100 shadow-lg"
	>
		<div class="text-2xl text-gray-700">
			{#if isEditingUsername}
				<input class="field" bind:value={user.username} />
				<button class="btn-primary" on:click={endEditUsername}>Save</button>
			{:else}
				<span class="">{user.username}</span>
				<button class="btn-primary" on:click={startEditUsername}>Change</button>
			{/if}
		</div>
		

		<div class="text-2xl text-gray-700">
			{#if isEditingEmail}
				<input class="field" bind:value={user.email} />
				<button class="btn-primary" on:click={endEditEmail}>Save</button>
			{:else}
				{user.email}
				<button class="btn-primary" on:click={startEditEmail}>Change</button>
			{/if}
		</div>

		<a href="/user/modify" class="btn-primary mt-6">Change password</a>

		<div class="flex-grow flex flex-col items-center justify-center">
			<div class="min-w-0">
				<img src="coin2.png" alt="coin" class="object-contain w-60" />
			</div>
			<div class="text-7xl">{user.coins}</div>
		</div>
	</div>
</div>
