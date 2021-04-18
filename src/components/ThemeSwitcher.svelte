<script lang="ts">
	import { mode } from '../stores';

	const handleClick = () => ($mode = $mode === 'dark' ? 'light' : 'dark');
</script>

<button on:click={handleClick} class={$mode}>{$mode === 'light' ? '🌞' : '🌙'} {$mode} mode</button>

<style lang="scss">
	button {
		text-transform: capitalize;
		display: flex;
		align-items: center;
		justify-content: space-between;
		background: transparent;
		border: none;
	}
</style>
