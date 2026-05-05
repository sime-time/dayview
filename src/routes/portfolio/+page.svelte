<script lang="ts">
import eventUgcCover from "$lib/assets/event-ugc/event-ugc.jpeg";
import crystalCover from "$lib/assets/crystal-signature-events/gala-ballroom-wide-1.webp";

const caseStudies = [
	{
		tag: "Airbnb Villa",
		title: "Room and view storytelling",
		description:
			"A full visual package covering bedrooms, bathrooms, detail moments, and perspective shots for listing performance.",
		href: "/portfolio/airbnb-villa",
		imageSrc: "/pics/faithbed.webp",
		imageAlt: "Bedroom frame from Airbnb villa project",
	},
	{
		tag: "Event UGC",
		title: "Pop-up campaign content and analytics",
		description:
			"Organic event content strategy and short-form execution across four event brands, with measurable follower and engagement growth.",
		href: "/portfolio/event-ugc",
		imageSrc: eventUgcCover,
		imageAlt: "Event UGC creator shot from Chicago pop-up campaign",
	},
	{
		tag: "event design",
		title: "crystal signature events operations + design",
		description:
			"vip event design and operations support across ferrari, indy 500, rose awards, member's mark, nba all-stars, weddings, and corporate experiences.",
		href: "/portfolio/crystal-signature-events",
		imageSrc: crystalCover,
		imageAlt: "gala ballroom setup for crystal signature events",
	},
];
</script>

<svelte:head>
	<title>portfolio | dayview</title>
	<meta
		name="description"
		content="case studies for hospitality photography and event UGC by Dayanna."
	/>
</svelte:head>

<main class="portfolio-index">
	<div class="shell">
		<a class="back-link" href="/">back to home</a>

		<header class="index-head">
			<p class="eyebrow">portfolio</p>
			<h1>case studies in hospitality, event ugc, and event design</h1>
			<p>
				a focused body of work blending creative direction, short-form production, and strategy-led
				content performance.
			</p>
		</header>

		<section class="project-grid" aria-label="Case studies">
			{#each caseStudies as caseStudy}
				<article class="project-card">
					<img src={caseStudy.imageSrc} alt={caseStudy.imageAlt} loading="lazy" />
					<div class="card-copy">
						<p class="tag">{caseStudy.tag}</p>
						<h2>{caseStudy.title}</h2>
						<p>{caseStudy.description}</p>
						<a class="cta" href={caseStudy.href}>open case study</a>
					</div>
				</article>
			{/each}
		</section>
	</div>
</main>

<style>
	.portfolio-index {
		min-height: 100dvh;
		padding: clamp(1.2rem, 2vw, 2rem) 1rem clamp(3rem, 7vw, 4.6rem);
		background: linear-gradient(to bottom, var(--color-accent) 0%, #ff8fd4 100%);
	}

	.shell {
		max-width: 1140px;
		margin: 0 auto;
		padding: clamp(1.2rem, 2.7vw, 2rem);
		border-radius: 30px;
		background: #ffffff;
	}

	.back-link {
		display: inline-flex;
		margin-bottom: 1.5rem;
		font-family: var(--font-sans);
		font-weight: 700;
		font-size: 0.92rem;
		letter-spacing: 0.02em;
		color: #6a1547;
	}

	.index-head {
		max-width: 64ch;
		margin-bottom: clamp(1.6rem, 2.8vw, 2.2rem);
	}

	.eyebrow {
		margin: 0 0 0.5rem;
		font-size: 0.82rem;
		font-family: var(--font-sans);
		font-weight: 800;
		letter-spacing: 0.14em;
		text-transform: uppercase;
		color: #5c0639;
	}

	h1 {
		margin: 0;
		font-family: var(--font-serif);
		font-size: clamp(2.1rem, 5vw, 4.2rem);
		line-height: 0.98;
		font-weight: 500;
		letter-spacing: -0.03em;
	}

	.index-head p {
		font-family: var(--font-sans);
		font-size: 1.05rem;
		line-height: 1.6;
		font-weight: 500;
		color: #2d1622;
	}

	.project-grid {
		display: grid;
		grid-template-columns: 1fr;
		gap: 1rem;
	}

	.project-card {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: clamp(1rem, 2.3vw, 1.8rem);
		padding: 0.9rem;
		border-radius: 22px;
		background: #fff7fc;
	}

	.project-card img {
		width: 100%;
		height: 100%;
		max-height: 520px;
		object-fit: cover;
		border-radius: 18px;
	}

	.card-copy {
		display: flex;
		flex-direction: column;
		justify-content: center;
		gap: 0.8rem;
	}

	.tag {
		margin: 0;
		align-self: flex-start;
		padding: 0.32rem 0.72rem;
		border-radius: 999px;
		background: #ffe4f3;
		font-family: var(--font-sans);
		font-size: 0.78rem;
		text-transform: uppercase;
		font-weight: 800;
		letter-spacing: 0.05em;
		color: #7a0d4f;
	}

	h2 {
		margin: 0;
		font-family: var(--font-sans);
		font-size: clamp(1.6rem, 2.6vw, 2.3rem);
		line-height: 1.08;
		font-weight: 800;
	}

	.card-copy p {
		margin: 0;
		font-family: var(--font-sans);
		font-size: 1rem;
		line-height: 1.58;
		color: #301522;
	}

	.cta {
		display: inline-flex;
		align-self: flex-start;
		margin-top: 0.25rem;
		padding: 0.72rem 1rem;
		border-radius: 999px;
		background: #160a12;
		color: #ffffff;
		font-family: var(--font-sans);
		font-size: 0.89rem;
		font-weight: 800;
	}

	@media (max-width: 900px) {
		.project-card {
			grid-template-columns: 1fr;
		}
	}
</style>
