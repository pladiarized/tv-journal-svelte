<script>
	import ShowInput from "./ShowInput.svelte";

	const submitShow = show => {
		console.log(show);
	};
</script>

<div class="main">
	<h1>
		TV Journal
	</h1>

	<ShowInput on:submitShow={
		e => submitShow(e.detail.show)
	} />
</div>

<style>

	.main {
		max-width: 500px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

</style>