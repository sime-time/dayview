<script lang="ts">
import eventUgcCover from "$lib/assets/event-ugc/oktoberfest.jpeg";
import crystalCover from "$lib/assets/crystal-signature-events/gala-ballroom-wide-1.webp";
</script>

<section class="portfolio" id="portfolio" aria-label="Portfolio section">
	<div class="portfolio-inner">
		<div class="portfolio-head">
			<div>
				<p class="eyebrow">Featured Work</p>
				<h2>portfolio</h2>
			</div>
			<p class="intro">
				built to help boutique stays book faster through intentional room, detail, and view photography.
			</p>
		</div>

		<div class="case-study">
			<div class="case-copy">
				<p class="tag">Airbnb Case Study</p>
				<h3>villa interiors + guest experience visuals</h3>
				<p class="description">
					a complete photo set from one Airbnb project, focused on bedrooms, bathrooms, living details,
					and the atmosphere guests feel when they arrive.
				</p>
				<a class="case-cta" href="/portfolio/airbnb-villa">view full case study</a>
			</div>

			<div class="featured-media">
				<img src="/pics/masterbedroom.webp" alt="Master bedroom frame from the Airbnb project" loading="lazy" />
			</div>
		</div>

		<article class="secondary-case" aria-label="Event UGC case study preview">
			<img src={eventUgcCover} alt="Crowd at Oktoberfest Chicago event" loading="lazy" />
			<div class="secondary-copy">
				<p class="tag">Event UGC Case Study</p>
				<h3>pop-up event content + performance analytics</h3>
				<p class="description">
					organic event marketing across four brands, including viral posts and nearly 3,000 new
					followers in one month for Frosty's New York.
				</p>
				<a class="case-cta" href="/portfolio/event-ugc">view event UGC case study</a>
			</div>
		</article>

		<article class="secondary-case" aria-label="crystal signature events case study preview">
			<img src={crystalCover} alt="gala ballroom setup for crystal signature events" loading="lazy" />
			<div class="secondary-copy">
				<p class="tag">event design case study</p>
				<h3>vip event operations + experiential design</h3>
				<p class="description">
					event designer support across ferrari, indy 500, rose awards, member's mark, nba all-stars,
					weddings, and corporate events through crystal signature events.
				</p>
				<a class="case-cta" href="/portfolio/crystal-signature-events">view event design case study</a>
			</div>
		</article>
	</div>
</section>

<style>
	.portfolio {
		position: relative;
		z-index: 2;
		padding: 0 1rem clamp(3.2rem, 6vw, 5rem);
		background: linear-gradient(to bottom, var(--color-accent) 0%, #ff8fd4 100%);
	}

	.portfolio-inner {
		position: relative;
		z-index: 3;
		max-width: 1280px;
		margin: 0 auto;
		padding: clamp(1.5rem, 3vw, 2.3rem);
		border-radius: 32px;
		background: #ffffff;
	}

	.portfolio-head {
		display: grid;
		grid-template-columns: 1fr auto;
		gap: 1.5rem;
		align-items: end;
		margin-bottom: clamp(1.8rem, 3.2vw, 2.8rem);
	}

	.eyebrow {
		margin: 0 0 0.6rem;
		font-family: var(--font-sans);
		font-size: 0.83rem;
		letter-spacing: 0.14em;
		text-transform: uppercase;
		font-weight: 700;
		color: #5c0639;
	}

	h2 {
		margin: 0;
		font-family: var(--font-serif);
		font-style: normal;
		font-size: clamp(2rem, 5.8vw, 4.5rem);
		line-height: 0.95;
		letter-spacing: -0.03em;
		font-weight: 500;
		color: var(--color-text);
	}

	.intro {
		margin: 0;
		max-width: 30ch;
		font-family: var(--font-sans);
		font-size: 1.12rem;
		line-height: 1.5;
		font-weight: 600;
		color: var(--color-text);
	}

	.case-study {
		display: grid;
		grid-template-columns: 1.05fr 1fr;
		gap: clamp(1.2rem, 3vw, 2rem);
		align-items: center;
		margin-bottom: clamp(1.2rem, 3vw, 1.9rem);
		padding: clamp(0.8rem, 1.6vw, 1rem);
		border-radius: 20px;
		background: #fff6fb;
	}

	.case-copy {
		display: flex;
		flex-direction: column;
		gap: 0.9rem;
	}

	h3 {
		margin: 0;
		font-family: var(--font-sans);
		font-size: clamp(1.8rem, 2.9vw, 2.9rem);
		line-height: 1.05;
		letter-spacing: -0.02em;
		font-weight: 700;
		color: var(--color-text);
	}

	.description {
		margin: 0;
		max-width: 44ch;
		font-family: var(--font-sans);
		font-size: 1.03rem;
		line-height: 1.58;
		font-weight: 500;
		color: #321422;
	}

	.case-cta {
		display: inline-flex;
		align-self: flex-start;
		margin-top: 0.4rem;
		padding: 0.72rem 1.05rem;
		border-radius: 9999px;
		background: #1a0a14;
		color: #ffffff;
		font-family: var(--font-sans);
		font-size: 0.9rem;
		font-weight: 800;
		letter-spacing: 0.02em;
		transition: transform 180ms ease, box-shadow 180ms ease;
	}

	.case-cta:hover {
		transform: translateY(-2px);
		box-shadow: 0 16px 28px rgb(12 5 10 / 0.2);
	}

	.featured-media {
		position: relative;
		min-height: 100%;
	}

	.featured-media img {
		display: block;
		width: 100%;
		height: 100%;
		max-height: 560px;
		object-fit: cover;
		border-radius: 24px;
		box-shadow: 0 22px 44px rgb(17 17 17 / 0.12);
	}

	.secondary-case {
		display: grid;
		grid-template-columns: minmax(280px, 500px) minmax(0, 1.2fr);
		gap: clamp(1.5rem, 3.2vw, 2.6rem);
		align-items: center;
		padding: clamp(0.8rem, 1.6vw, 1rem);
		border-radius: 20px;
		background: #fff6fb;
	}

	.secondary-case + .secondary-case {
		margin-top: clamp(0.9rem, 1.8vw, 1.2rem);
	}

	.secondary-case img {
		display: block;
		width: 100%;
		aspect-ratio: 4 / 5;
		object-fit: cover;
		border-radius: 14px;
		box-shadow: 0 16px 30px rgb(17 17 17 / 0.12);
	}

	.secondary-copy {
		display: grid;
		gap: 0.7rem;
		align-content: center;
		max-width: 70ch;
	}

	.secondary-copy .tag,
	.case-copy .tag {
		justify-self: start;
		width: fit-content;
	}

	.secondary-copy h3 {
		font-size: clamp(1.45rem, 2.4vw, 2.25rem);
		line-height: 1.12;
		max-width: 22ch;
	}

	.secondary-copy .description {
		max-width: 52ch;
	}

	.secondary-copy .case-cta {
		justify-self: start;
		width: fit-content;
	}

	.tag {
		align-self: flex-start;
		margin: 0;
		padding: 0.36rem 0.82rem;
		border-radius: 9999px;
		background: var(--color-accent-soft);
		font-family: var(--font-sans);
		font-size: 0.79rem;
		font-weight: 700;
		letter-spacing: 0.05em;
		text-transform: uppercase;
		color: #7a0d4f;
	}

	@media (max-width: 1080px) {
		.portfolio {
			padding-top: clamp(2.6rem, 7vw, 4rem);
		}

		.portfolio-head {
			grid-template-columns: 1fr;
			align-items: start;
		}

		.case-study {
			grid-template-columns: 1fr;
		}

		.secondary-case {
			grid-template-columns: 1fr;
		}

		.secondary-copy {
			order: 1;
		}

		.secondary-case img {
			order: 2;
		}
	}

	@media (max-width: 680px) {
		.portfolio {
			padding: 2.2rem 0.65rem clamp(2.4rem, 8vw, 3rem);
		}

		.portfolio-inner {
			padding: 1.1rem;
			border-radius: 24px;
		}

		.secondary-case img {
			aspect-ratio: 3 / 4;
		}

		.secondary-copy h3 {
			font-size: 1.55rem;
		}

		h3 {
			font-size: 1.72rem;
		}

		h2 {
			font-size: clamp(2.7rem, 13vw, 3.7rem);
			font-weight: 400;
			line-height: 0.92;
		}
	}
</style>
