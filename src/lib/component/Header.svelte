<script lang="ts">
	import { base } from '$app/paths';
	import Toggle from '$lib/component/Toggle.svelte';
	import Logo from './Logo.svelte';
</script>

<nav>
	<a href="{base}/" class="title">
		<Logo />
	</a>
	<ul class="links">
		<li><a href="{base}/about">About</a></li>
		<li><a href="{base}/contact">Contact</a></li>
	</ul>
	<Toggle />
</nav>

<style>
	nav {
		padding-block: var(--size-7);
	}
	ul {
		align-items: center;
	}
	.links {
		margin-block: var(--size-7);
	}
	a {
		color: inherit;
		text-decoration: none;
	}
	@media (min-width: 768px) {
		nav {
			display: flex;
			justify-content: space-between;
		}
		.links {
			display: flex;
			gap: var(--size-7);
			margin-block: 0;
		}
	}
</style>
