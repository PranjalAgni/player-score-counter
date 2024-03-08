<script lang="ts">
	export let playerName: string;
	export let playerScore: number;

	function incrementPlayerScore() {
		playerScore += 1;
	}

	function decrementPlayerScore() {
		if (playerScore < 0) return;
		playerScore -= 1;
	}
</script>

<div>
	<h2 class="center">{playerName}</h2>
	<h3 class="center">{playerScore}</h3>
	<div class="container">
		<button class="button" on:click={incrementPlayerScore}>Up</button>
		<button class="button" on:click={decrementPlayerScore}>Down</button>
	</div>
	{#if playerScore < 0}
		<p>Can't go less than this now</p>
	{/if}
</div>

<style>
	.center {
		text-align: center;
	}
	.container {
		display: flex;
		flex-direction: column;
		flex-wrap: wrap;
	}
	.button {
		margin: 5px;
		width: 100%;
	}
</style>
