<script lang="ts">
	import type { Snippet } from 'svelte';
	import type { LayoutData } from './$types';

	let { data, children }: { data: LayoutData; children: Snippet } = $props();
</script>

<div>
	<aside>
		<nav>
			<a href="/contador">Contador</a>
		</nav>
	</aside>
	<main>
		{@render children()}
	</main>
</div>

<style>
	:root {
		font-family:
			Roboto,
			system-ui,
			-apple-system,
			BlinkMacSystemFont,
			'Segoe UI',
			Oxygen,
			Ubuntu,
			Cantarell,
			'Open Sans',
			'Helvetica Neue',
			sans-serif;
	}
	div {
		display: flex;
	}
	main {
		display: grid;
		place-content: center;
	}
	aside {
		flex-basis: 14rem;
		padding: var(--padding, 1rem);
	}
</style>
