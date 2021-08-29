<script lang="ts">
  import { onMount } from "svelte"

  export let name: string

  onMount(() => {
    fetch(
      `https://api.openweathermap.org/data/2.5/onecall?lat=40.356034699999995&lon=-111.75281389999999&appid=875d258f134df1f1b63378278de4e2e8`
    )
      .then((res) => res.json())
      .then(console.log)
  })
</script>

<main>
	<h1>Weather</h1>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
