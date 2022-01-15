<script>
	import ShowInput from "./ShowInput.svelte";
	import ShowList from "./ShowList.svelte";

	let shows = localStorage.getItem("shows") ? JSON.parse(localStorage.getItem("shows")) : [];

	const submitShow = show => {
		const updatedShows = [...shows, show];
		localStorage.setItem("shows", JSON.stringify(updatedShows));
		shows = updatedShows;
	};
</script>

<div class="main">
	<h1>
		TV Journal
	</h1>

	<ShowInput on:submitShow={
		e => submitShow(e.detail.show)
	} />

	<ShowList shows={
		shows
	} />
</div>

<style>
	.main {
    width: 500px;
    max-width: 100%;
    padding: 1em;
    margin: auto;
    text-align: center;
  }
	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}
</style>