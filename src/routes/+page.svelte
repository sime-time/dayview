<script lang="ts">
import About from "$lib/components/About.svelte";
import Contact from "$lib/components/Contact.svelte";
import Footer from "$lib/components/Footer.svelte";
import Hero from "$lib/components/Hero.svelte";
import Portfolio from "$lib/components/Portfolio.svelte";
</script>

<svelte:head>
	<title>dayview</title>
	<meta
		name="description"
		content="portfolio of dayanna gomez, social media content creator"
	/>
</svelte:head>


<Hero />
<Portfolio />
<About />
<Contact />
<Footer />
