<script lang="ts">
	export let value: number = 0;

	let randomValue: number = 0;

	function getRandomInt(min: number, max: number) {
		const positive = Math.random() > 0.5 ? 1 : -1;
		return positive * Math.floor(Math.random() * (max - min) + min);
	}

	function addRandomNumber() {
		randomValue = getRandomInt(1, 100);
	}
</script>

<div>
	<button class="blue" on:click={addRandomNumber}>Click Me!</button>
	<span data-testid="value" class={value < 0 ? 'red' : 'green'}>{value}</span>
	<div data-testid="random-value" class="hidden">{randomValue}</div>
</div>

<style>
	.hidden {
		display: none;
	}
</style>