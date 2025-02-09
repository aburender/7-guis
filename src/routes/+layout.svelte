<script lang="ts">
	import type { Snippet } from 'svelte';
	import type { LayoutData } from './$types';
	import '$lib/style.css';

	let { data, children }: { data: LayoutData; children: Snippet } = $props();
</script>

<div>
	<aside>
		<nav>
			<ul>
				<li>
					<a href="/contador">Contador</a>
				</li>
				<li>
					<a href="/convertidor-temperatura">convertidor de temperatura</a>
				</li>
			</ul>
		</nav>
	</aside>
	<main>
		{@render children()}
	</main>
</div>

<style>
	div {
		display: flex;
	}
	main {
		display: grid;
		place-content: center;
		place-items: center;
		height: 100dvh;
		flex: 1;
	}
	aside {
		flex-basis: 20rem;
		padding: var(--padding, 1rem);
	}

	a {
		text-transform: capitalize;
	}
</style>
