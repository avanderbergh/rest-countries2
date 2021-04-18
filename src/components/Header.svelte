<script>
	import ThemeSwitcher from './ThemeSwitcher.svelte';
</script>

<header>
	<h1>Where in the world?</h1>
	<ThemeSwitcher />
</header>

<style lang="scss">
	header {
		position: sticky;
		top: 0;
		padding: 0.5rem 1rem;
		display: flex;
		justify-content: space-between;
		background-color: var(--background);
		transition: all 1s;
		box-shadow: var(--shadow-level-1);

		h1 {
			font-size: 1rem;
		}
	}
</style>
