<script lang="ts">
import analytics from "$lib/assets/event-ugc/analytics.jpeg";
import eventUgc from "$lib/assets/event-ugc/event-ugc.jpeg";
import followers from "$lib/assets/event-ugc/followers.jpeg";
import oktoberfest from "$lib/assets/event-ugc/oktoberfest.jpeg";
import pumpkinpatch from "$lib/assets/event-ugc/pumpkinpatch.jpeg";
import watchtime from "$lib/assets/event-ugc/watchtime.jpeg";
import watchtime2 from "$lib/assets/event-ugc/watchtime2.jpeg";

const campaignGallery = [
	{
		src: eventUgc,
		alt: "Event UGC creator on location at pop-up event",
	},
	{
		src: oktoberfest,
		alt: "Oktoberfest Chicago event UGC moment",
	},
	{
		src: pumpkinpatch,
		alt: "Jack's Pumpkin Pop-Up event campaign visual",
	},
];

const resultsGallery = [
	{
		src: followers,
		alt: "Follower growth analytics from event UGC campaign",
	},
	{
		src: watchtime,
		alt: "Watch time analytics from short-form event content",
	},
	{
		src: watchtime2,
		alt: "Additional audience retention analytics from campaign",
	},
	{
		src: analytics,
		alt: "Performance analytics summary showing engagement results",
	},
];
</script>

<svelte:head>
	<title>event ugc case study | dayview</title>
	<meta
		name="description"
		content="case study on event UGC strategy, production, and analytics across major pop-up brands in Chicago and New York."
	/>
</svelte:head>

<main class="case-page">
	<div class="shell">
		<a class="back-link" href="/portfolio">Back to portfolio</a>

		<header class="hero">
			<p class="eyebrow">Case Study</p>
			<h1>Event UGC for pop-up experiences</h1>
			<p>
				A digital marketing project with V5 Group focused on organic event marketing for
				large-scale pop-up experiences in Chicago and New York City.
			</p>
		</header>

		<section class="brief" aria-label="Project brief">
			<div>
				<h2>Scope and execution</h2>
				<p>
					Managed four event brands - Halloween Town, Jack's Pumpkin Pop-Up, Oktoberfest Chicago,
					and Frosty's New York - including content strategy, posting schedules, shot lists, and
					platform-specific brand voice.
				</p>
			</div>
			<div>
				<h2>Production approach</h2>
				<ul>
					<li>Shot, edited, and produced short-form vertical videos</li>
					<li>Used text overlays to increase FOMO and ticket discovery</li>
					<li>Matched transitions to track rhythm to improve retention</li>
					<li>Prioritized native iPhone footage for algorithm-fit authenticity</li>
				</ul>
			</div>
		</section>

		<section class="gallery" aria-label="Event UGC campaign gallery">
			{#each campaignGallery as image}
				<figure>
					<img src={image.src} alt={image.alt} loading="lazy" />
				</figure>
			{/each}
		</section>

		<section class="impact" aria-label="Campaign performance">
			<div class="impact-copy">
				<h2>Performance impact</h2>
				<p>
					Through testing, iteration, and performance analysis, this campaign generated multiple viral
					posts and grew the Frosty's New York account by nearly 3,000 followers in one month.
				</p>
				<p>
					That account also outperformed other Frosty's pop-ups in ticket sales and engagement,
					showing how targeted, authentic UGC can drive real-world results.
				</p>
			</div>

			<div class="results-grid">
				{#each resultsGallery as result}
					<figure>
						<img src={result.src} alt={result.alt} loading="lazy" />
					</figure>
				{/each}
			</div>
		</section>

		<section class="cta-block" aria-label="Book event UGC support">
			<h2>Planning a pop-up or seasonal event?</h2>
			<p>
				Book event UGC support for strategy, shot lists, and short-form content that drives awareness
				and ticket action.
			</p>
			<a href="/contact">Book event UGC</a>
		</section>
	</div>
</main>

<style>
	.case-page {
		min-height: 100dvh;
		padding: clamp(1.2rem, 2vw, 2rem) 1rem clamp(3rem, 7vw, 4.8rem);
		background: linear-gradient(to bottom, var(--color-accent) 0%, #ff8fd4 100%);
	}

	.shell {
		max-width: 1180px;
		margin: 0 auto;
		padding: clamp(1.2rem, 2.7vw, 2rem);
		border-radius: 30px;
		background: #ffffff;
	}

	.back-link {
		display: inline-flex;
		margin-bottom: 1.35rem;
		font-family: var(--font-sans);
		font-weight: 700;
		font-size: 0.92rem;
		letter-spacing: 0.02em;
		color: #6a1547;
	}

	.hero {
		max-width: 74ch;
		margin-bottom: clamp(1.7rem, 3.3vw, 2.7rem);
	}

	.eyebrow {
		margin: 0 0 0.5rem;
		font-family: var(--font-sans);
		font-size: 0.82rem;
		font-weight: 800;
		letter-spacing: 0.14em;
		text-transform: uppercase;
		color: #5c0639;
	}

	h1 {
		margin: 0;
		font-family: var(--font-serif);
		font-size: clamp(2rem, 5vw, 4rem);
		line-height: 0.98;
		font-weight: 500;
		letter-spacing: -0.03em;
	}

	.hero p {
		font-family: var(--font-sans);
		font-size: 1.04rem;
		line-height: 1.6;
		font-weight: 500;
		color: #321422;
	}

	.brief {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: clamp(1rem, 2.4vw, 1.8rem);
		margin-bottom: clamp(1.4rem, 3vw, 2.1rem);
	}

	.brief div {
		padding: 1rem;
		border-radius: 16px;
		background: #fff7fc;
	}

	h2 {
		margin: 0 0 0.55rem;
		font-family: var(--font-sans);
		font-size: clamp(1.35rem, 2.4vw, 1.8rem);
		line-height: 1.12;
		font-weight: 800;
	}

	.brief p,
	.impact-copy p,
	.cta-block p,
	li {
		margin: 0;
		font-family: var(--font-sans);
		font-size: 1rem;
		line-height: 1.58;
		color: #301522;
	}

	ul {
		margin: 0;
		padding-left: 1.2rem;
		display: grid;
		gap: 0.35rem;
	}

	.gallery {
		display: grid;
		grid-template-columns: repeat(3, minmax(0, 1fr));
		gap: clamp(0.7rem, 1.6vw, 1.1rem);
		margin-bottom: clamp(1.5rem, 3vw, 2.2rem);
	}

	figure {
		margin: 0;
	}

	figure img {
		display: block;
		width: 100%;
		aspect-ratio: 4 / 5;
		object-fit: cover;
		border-radius: 14px;
		box-shadow: 0 16px 30px rgb(17 17 17 / 0.1);
	}

	.impact {
		display: grid;
		grid-template-columns: 1fr 1.1fr;
		gap: clamp(1rem, 2.4vw, 1.8rem);
		margin-bottom: clamp(1.5rem, 3vw, 2.3rem);
	}

	.impact-copy {
		padding: 1rem;
		border-radius: 16px;
		background: #fff7fc;
		display: grid;
		gap: 0.7rem;
	}

	.results-grid {
		display: grid;
		grid-template-columns: repeat(2, minmax(0, 1fr));
		gap: 0.8rem;
	}

	.results-grid img {
		aspect-ratio: 1 / 1;
	}

	.cta-block {
		padding: clamp(1rem, 2.2vw, 1.7rem);
		border-radius: 16px;
		background: #160a12;
		color: #ffffff;
	}

	.cta-block h2,
	.cta-block p {
		color: #ffffff;
	}

	.cta-block a {
		display: inline-flex;
		margin-top: 0.85rem;
		padding: 0.72rem 1rem;
		border-radius: 999px;
		background: #ffb6df;
		font-family: var(--font-sans);
		font-size: 0.9rem;
		font-weight: 800;
		color: #270718;
	}

	@media (max-width: 960px) {
		.brief,
		.impact {
			grid-template-columns: 1fr;
		}

		.gallery {
			grid-template-columns: repeat(2, minmax(0, 1fr));
		}
	}

	@media (max-width: 620px) {
		.gallery,
		.results-grid {
			grid-template-columns: 1fr;
		}
	}
</style>
