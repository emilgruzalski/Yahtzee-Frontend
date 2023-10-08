<script lang="ts">
	import '../app.css';
</script>

<div class="h-screen flex flex-col">
	<div class="flex items-center py-2 px-4 shadow-sm border-b-2 border-gray-300">
		<a href="/" class="text-3xl font-thin font-mono">Poker Dice</a>
		<a href="/login" class="ms-auto btn-primary-full">
			Login
		</a>
	</div>
	<div class="flex-grow">
		<slot />
	</div>
</div>

<style lang='postcss'>
	:global(.field) {
		@apply border-2 border-gray-300 focus:outline-gray-400 rounded-md p-2
	}

	:global(.btn-primary) {
		@apply border-2 border-blue-400 bg-blue-100 hover:bg-blue-200 text-black rounded-md px-3 py-2 text-center
	}

	:global(.btn-primary-full) {
		@apply bg-blue-700 hover:bg-blue-700/80 text-white rounded-md p-3
	}
</style>
