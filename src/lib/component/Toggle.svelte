<script lang="ts">
	import { fly } from 'svelte/transition';
	import { theme, toggleTheme } from '$lib/store/theme';
</script>

<button on:click={toggleTheme} aria-label="Toggle theme">
	{#if $theme === 'dark'}
		<div in:fly={{ y: 10 }}>
			😎
			<span>Light</span>
		</div>
	{:else}
		<div in:fly={{ y: -10 }}>
			🌙
			<span>Dark</span>
		</div>
	{/if}
</button>

<style>
	button {
		font-weight: inherit;
		background: none;
		border: none;
		box-shadow: none;
		overflow: hidden;
	}
	button > * {
		display: flex;
		gap: var(--size-2);
	}
</style>
