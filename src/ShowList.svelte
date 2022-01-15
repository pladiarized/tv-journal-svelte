<script>
    export let shows;
</script>

{#each shows as show (show.title)}
    <div>
        <h2>{show.title}</h2>
        <p>Your Rating: {show.rating}</p>
    </div>
{/each}

<style>
    div {
      text-align: left;
      padding-bottom: 10px;
      border-bottom: 1px solid black;
    }
  </style>