<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';
	import '@fontsource-variable/playfair-display';
	import '@fontsource-variable/mulish';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<style>
	:global(:root) {
		--color-primary: #000000;
		--color-surface: #ffffff;
		--color-surface-low: #fafafa;
		--color-accent: #ff66c4;
		--color-accent-soft: #ffe0f2;
		--color-text: #111111;
		--color-muted: #666666;
		--shadow-ambient: 0 20px 56px rgb(17 17 17 / 0.04);
		--font-serif: 'Playfair Display Variable', 'Playfair Display', serif;
		--font-sans: 'Mulish Variable', 'Mulish', sans-serif;
	}

	:global(*) {
		box-sizing: border-box;
	}

	:global(html),
	:global(body) {
		margin: 0;
		padding: 0;
		background: var(--color-surface);
		color: var(--color-text);
		font-family: var(--font-sans);
	}

	:global(a) {
		color: inherit;
		text-decoration: none;
	}
</style>

{@render children()}
