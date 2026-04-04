<script lang="ts">
import favicon from "$lib/assets/favicon.svg";
import "@fontsource-variable/playfair-display";
import "@fontsource-variable/mulish";

let { children } = $props();
</script>

<svelte:head>
	<title>dayview</title>
	<meta
		name="description"
		content="Portfolio for Day, a social media manager and videographer creating short-form content for brands and personal brands. Book a call to plan your next campaign."
	/>
	<meta property="og:title" content="dayview" />
	<meta
		property="og:description"
		content="Portfolio for Day, a social media manager and videographer creating short-form content for brands and personal brands. Book a call to plan your next campaign."
	/>
	<meta property="og:type" content="website" />
	<meta name="twitter:card" content="summary" />
	<meta name="twitter:title" content="dayview" />
	<meta
		name="twitter:description"
		content="Portfolio for Day, a social media manager and videographer creating short-form content for brands and personal brands. Book a call to plan your next campaign."
	/>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children()}

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
		--nav-scroll-offset: 4.3rem;
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

	:global(html) {
		scroll-padding-top: var(--nav-scroll-offset);
	}

	:global(section[id]) {
		scroll-margin-top: var(--nav-scroll-offset);
	}

	:global(a) {
		color: inherit;
		text-decoration: none;
	}

	@media (max-width: 900px) {
		:global(:root) {
			--nav-scroll-offset: 3.1rem;
		}
	}
</style>
