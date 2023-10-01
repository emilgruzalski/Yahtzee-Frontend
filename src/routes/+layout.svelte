<script lang="ts">
	import '../app.css';
</script>

<div class="h-screen flex flex-col">
	<div class="flex items-center py-2 px-4 shadow-sm border-b-2 border-gray-300">
		<a href="/" class="text-3xl font-thin font-mono">Poker Dice</a>
		<a href="/login" class="ms-auto border bg-gray-100 border-gray-300 hover:bg-gray-200 p-2 px-6 rounded-md">
			Login
		</a>
	</div>
	<div class="flex-grow">
		<slot />
	</div>
</div>
