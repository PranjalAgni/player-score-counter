<script>
	import PlayerScore from "../components/PlayerScore.svelte";
	let player1Score = 0;
	let player2Score = 0;
        console.log("Svelte is so cool");

	function reset() {
		player1Score = 0;
		player2Score = 0;
	}
</script>

<main>
	<PlayerScore bind:playerScore={player1Score} playerName="Player 1" />
	<PlayerScore bind:playerScore={player2Score} playerName="Player 2" />
	<input type="reset" class="mt" on:click={reset} />
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
	.mt {
		margin-top: 2em;
	}
</style>
