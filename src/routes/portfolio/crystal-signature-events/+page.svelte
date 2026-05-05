<script lang="ts">
import ballroomOne from "$lib/assets/crystal-signature-events/gala-ballroom-wide-1.webp";
import ballroomTwo from "$lib/assets/crystal-signature-events/gala-ballroom-wide-2.webp";
import ballroomThree from "$lib/assets/crystal-signature-events/gala-ballroom-wide-3.webp";
import roseAwards from "$lib/assets/crystal-signature-events/rose-awards-stage-screens.webp";
import ferrariOne from "$lib/assets/crystal-signature-events/live-painting-race-car-1.webp";
import ferrariTwo from "$lib/assets/crystal-signature-events/live-painting-race-car-2.webp";
import centerpieceOne from "$lib/assets/crystal-signature-events/event-table-centerpiece-15-1.webp";
import centerpieceTwo from "$lib/assets/crystal-signature-events/event-table-centerpiece-15-4.webp";
import cakeAndCenterpieces from "$lib/assets/crystal-signature-events/wedding-cake-and-centerpieces.webp";
import barSetup from "$lib/assets/crystal-signature-events/gala-backlit-bar.webp";

const portfolioGallery = [
	{ src: ballroomOne, alt: "wide ballroom production setup" },
	{ src: roseAwards, alt: "rose awards stage and screen design" },
	{ src: ferrariOne, alt: "ferrari event live painting activation" },
	{ src: centerpieceOne, alt: "formal centerpiece styling for vip table" },
	{ src: barSetup, alt: "backlit gala bar staging" },
	{ src: cakeAndCenterpieces, alt: "wedding cake and floral centerpiece design" },
	{ src: ballroomTwo, alt: "secondary ballroom angle for event reveal" },
	{ src: ferrariTwo, alt: "race car event audience engagement moment" },
	{ src: ballroomThree, alt: "large scale ballroom final guest-ready scene" },
	{ src: centerpieceTwo, alt: "elevated table centerpiece detail" },
];
</script>

<svelte:head>
	<title>crystal signature events case study | dayview</title>
	<meta
		name="description"
		content="case study showcasing event design and vip operations support for crystal signature events across luxury and corporate experiences."
	/>
</svelte:head>

<main class="case-page">
	<div class="shell">
		<a class="back-link" href="/portfolio">back to portfolio</a>

		<header class="hero">
			<p class="eyebrow">case study</p>
			<h1>crystal signature events: vip operations + event design</h1>
			<p>
				as an event designer supporting crystal signature events, dayanna helped execute guest-facing
				experiences across ferrari, indy 500, rose awards, member's mark, nba all-stars, weddings,
				and additional corporate events.
			</p>
		</header>

		<section class="brief" aria-label="project scope and responsibilities">
			<div>
				<h2>scope</h2>
				<p>
					worked across luxury and high-volume event formats, coordinating visual design details and
					operational flow to keep each guest experience polished, on-brand, and production-ready.
				</p>
			</div>
			<div>
				<h2>responsibilities</h2>
				<ul>
					<li>vip event operations support across multi-team productions</li>
					<li>event design styling for tablescapes, bars, stages, and signature moments</li>
					<li>on-site execution for weddings, brand activations, and corporate galas</li>
					<li>detail coordination to protect guest flow and brand presentation</li>
				</ul>
			</div>
		</section>

		<section class="gallery" aria-label="crystal signature events image gallery">
			{#each portfolioGallery as image}
				<figure>
					<img src={image.src} alt={image.alt} loading="lazy" />
				</figure>
			{/each}
		</section>

		<section class="cta-block" aria-label="book event design and marketing support">
			<h2>planning a high-touch event?</h2>
			<p>
				book support with someone who understands event design, guest operations, and content capture
				that supports real marketing outcomes.
			</p>
			<a href="/contact">book a strategy call</a>
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
		.brief {
			grid-template-columns: 1fr;
		}

		.gallery {
			grid-template-columns: repeat(2, minmax(0, 1fr));
		}
	}

	@media (max-width: 620px) {
		.gallery {
			grid-template-columns: 1fr;
		}
	}
</style>
