<script lang="ts">
	import { mode } from '../stores';
	import Header from '../components/Header.svelte';
	import CountryList from '../components/CountryList.svelte';
</script>

<main class={$mode}>
	<Header />
	<CountryList />
</main>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Nunito+Sans:wght@300;600;800&display=swap');

	:global(body) {
		--elements-dark: hsl(209, 23%, 22%);
		--elements-light: hsl(0, 0%, 100%);
		--background-dark: hsl(207, 26%, 17%);
		--background-light: hsl(0, 0%, 98%);
		--text-dark: hsl(0, 0%, 100%);
		--text-light: hsl(200, 15%, 8%);
		--input-light: hsl(0, 0%, 52%);

		--shadow-level-1: 0.1rem 0.1rem 0.5rem rgba(0, 0, 0, 0.1),
			-0.05rem -0.05rem 0.2rem rgba(0, 0, 0, 0.5);

		font-family: 'Nunito Sans', sans-serif;
		font-size: 14px;
		margin: 0;
		padding: 0;
		height: 100vh;
	}

	:global(button) {
		color: var(--text);
		font-size: 1rem;
		font-family: 'Nunito Sans', sans-serif;
		font-weight: 600;
		outline: none;
	}
	.dark {
		--elements: var(--elements-dark);
		--background: var(--background-dark);
		--text: var(--text-dark);
	}

	.light {
		--elements: var(--elements-light);
		--background: var(--background-light);
		--text: var(--text-light);
	}

	main {
		background-color: var(--background);
		color: var(--text);

		transition: background-color 1s, color 1s;
		width: 100vw;
	}
</style>
