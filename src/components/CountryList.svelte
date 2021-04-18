<script lang="ts">
	import CountryCard from './CountryCard.svelte';
	import { onMount } from 'svelte';

	let countries: any[] = [];

	onMount(async () => {
		const res = await fetch('https://restcountries.eu/rest/v2/all');
		countries = await res.json();
		console.log(countries);
	});
</script>

{#each countries as country}
	<CountryCard {country} />
{/each}
