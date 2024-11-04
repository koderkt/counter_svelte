<script lang="ts">
	let counter: number = $state(0);

	function increment(): void {
		counter++;
	}
	function decrement(): void {
		counter--;
	}
</script>

<div class="flex justify-center items-center h-screen bg-slate-500">
	<div class="bg-gray-100 p-6 rounded-lg shadow-lg flex flex-col items-center space-y-4">
		<input
			type="text"
			class="px-3 py-2 border border-gray-300 rounded-lg text-center bg-gray-50 text-gray-700"
			bind:value={counter}
			disabled
		/>
		<div class="flex space-x-4">
			<button
				class="px-4 py-2 bg-blue-500 text-white font-semibold rounded-lg hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-red-300"
				onclick={increment}
			>
				Increment
			</button>
			<button
				class="px-4 py-2 bg-blue-500 text-white font-semibold rounded-lg hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-red-300"
				onclick={decrement}
			>
				Decrement
			</button>
		</div>
	</div>
</div>
