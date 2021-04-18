<script lang="ts">
	import type { Country } from '../interfaces/Country';
	import CountryCard from './CountryCard.svelte';
	import { onMount } from 'svelte';

	let countries: Country[] = [];

	onMount(async () => {
		const res = await fetch('https://restcountries.eu/rest/v2/all');
		countries = await res.json();
	});
</script>

{#each countries as country}
	<CountryCard {country} />
{/each}
