<script lang="ts">
const gallery = [
	{
		src: "/pics/faithbed.webp",
		alt: "Primary bedroom shot with natural light",
	},
	{
		src: "/pics/masterbedroom.webp",
		alt: "Master bedroom composition with layered textiles",
	},
	{
		src: "/pics/guestbedroom.webp",
		alt: "Guest bedroom styled for comfort and clarity",
	},
	{
		src: "/pics/bedroomtv.webp",
		alt: "Bedroom television area and seating details",
	},
	{
		src: "/pics/guestbathroom.webp",
		alt: "Guest bathroom with clean fixture lines",
	},
	{
		src: "/pics/bathroomsinks.webp",
		alt: "Bathroom sink detail and mirror framing",
	},
	{ src: "/pics/shower.webp", alt: "Shower area with texture and contrast" },
	{
		src: "/pics/tvstation.webp",
		alt: "Living area media console and decor styling",
	},
	{
		src: "/pics/globe.webp",
		alt: "Decor detail for a lived-in hospitality feel",
	},
	{
		src: "/pics/toilet.webp",
		alt: "Bathroom utility composition for listing completeness",
	},
];

const videoScenes = [
	"Room walkthrough framing to show flow and size",
	"Window and balcony perspective clips focused on the view",
	"Slow motion detail cuts for premium listing reels",
];
</script>

<svelte:head>
	<title>Airbnb Villa Case Study | dayview</title>
	<meta
		name="description"
		content="Case study of an Airbnb villa photo and motion project focused on room storytelling and guest experience."
	/>
</svelte:head>

<main class="case-page">
	<div class="shell">
		<a class="back-link" href="/">Back to home</a>

		<header class="hero">
			<p class="eyebrow">Case Study</p>
			<h1>Airbnb villa: interiors, details, and guest-first framing</h1>
			<p>
				This project documents one Airbnb property from arrival impression through room-level detail,
				built to improve listing trust and visual consistency across booking platforms.
			</p>
		</header>

		<section class="brief" aria-label="Project brief">
			<div>
				<h2>Project brief</h2>
				<p>
					The goal was to make every key guest space feel clear, warm, and bookable. Coverage prioritized
					bedrooms, bathrooms, texture details, and angles that communicate scale without distortion.
				</p>
			</div>
			<div>
				<h2>Deliverables</h2>
				<ul>
					<li>10 edited stills for listing and social use</li>
					<li>Villa clips designed for short vertical edits</li>
					<li>Compositions planned around guest decision points</li>
				</ul>
			</div>
		</section>

		<section class="gallery" aria-label="Airbnb villa image gallery">
			{#each gallery as image}
				<figure>
					<img src={image.src} alt={image.alt} loading="lazy" />
				</figure>
			{/each}
		</section>

		<section class="cta-block" aria-label="Book hospitality shoot">
			<h2>Need visuals for your stay?</h2>
			<p>Book a hospitality photo and motion session tailored for Airbnb, villas, and boutique rentals.</p>
			<a href="/contact">Book hospitality shoot</a>
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
		max-width: 72ch;
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
