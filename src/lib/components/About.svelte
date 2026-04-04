<script lang="ts">
import aboutDay from "$lib/assets/about-day.webp";
</script>

<section class="about" id="about" aria-label="About section">
	<div class="about-inner">
		<div class="about-image-wrap">
			<img src={aboutDay} alt="Dayanna smiling portrait" />
		</div>

		<div class="about-content">
			<p class="eyebrow">About</p>
			<h2>meet dayanna</h2>
			<p class="about-copy">
				dayanna brings 3 years of direct sales experience and 4 years of videography and social
				media account management.
			</p>
			<p class="about-copy muted">
				she blends strategy with storytelling to create shortform content that drives visibility,
				engagement, and momentum for event promotion and personal brands.
			</p>

			<div class="badges" aria-label="Experience highlights">
				<span>3 years of direct sales</span>
				<span>social media strategy</span>
			</div>
		</div>
	</div>
</section>

<style>
	.about {
		padding: clamp(3.2rem, 6vw, 5.6rem) 1rem;
		background: var(--color-surface-low);
	}

	.about-inner {
		max-width: 1240px;
		margin: 0 auto;
		display: grid;
		grid-template-columns: minmax(320px, 520px) minmax(0, 1fr);
		gap: clamp(1.4rem, 4vw, 4.2rem);
		align-items: center;
		padding: clamp(1rem, 2vw, 1.6rem);
		border-radius: 30px;
		background: var(--color-surface-low);
	}

	.about-image-wrap {
		border-radius: 26px;
		overflow: hidden;
		background: var(--color-accent-soft);
		box-shadow: 0 30px 58px rgb(17 17 17 / 0.04);
	}

	.about-image-wrap img {
		display: block;
		width: 100%;
		height: auto;
		object-fit: cover;
	}

	.about-content {
		padding: clamp(0.2rem, 1vw, 0.8rem) clamp(0.2rem, 1vw, 0.6rem);
	}

	.eyebrow {
		margin: 0 0 0.7rem;
		font-family: var(--font-sans);
		font-size: 0.72rem;
		font-weight: 700;
		letter-spacing: 0.14em;
		text-transform: uppercase;
		color: var(--color-accent);
	}

	h2 {
		margin: 0 0 1.1rem;
		font-family: var(--font-serif);
		font-style: italic;
		font-size: clamp(2rem, 4.8vw, 4rem);
		line-height: 0.95;
		letter-spacing: -0.02em;
		font-weight: 500;
		color: var(--color-text);
	}

	.about-copy {
		margin: 0;
		max-width: 42ch;
		font-family: var(--font-sans);
		font-size: 1.03rem;
		line-height: 1.65;
		font-weight: 600;
		color: var(--color-text);
	}

	.about-copy + .about-copy {
		margin-top: 1rem;
	}

	.about-copy.muted {
		color: var(--color-muted);
		font-weight: 500;
	}

	.badges {
		display: flex;
		flex-wrap: wrap;
		gap: 0.72rem;
		margin-top: 1.5rem;
	}

	.badges span {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		padding: 0.52rem 0.9rem;
		border-radius: 9999px;
		background: var(--color-accent-soft);
		font-family: var(--font-sans);
		font-size: 0.83rem;
		font-weight: 700;
		letter-spacing: 0.02em;
		color: #7a0d4f;
	}

	@media (max-width: 980px) {
		.about-inner {
			grid-template-columns: 1fr;
			gap: 1.2rem;
		}

		.about-content {
			padding: 0.35rem 0.2rem;
		}
	}

	@media (max-width: 680px) {
		.about {
			padding: clamp(2.4rem, 7vw, 3.2rem) 0.65rem;
		}

		h2 {
			font-size: clamp(2.2rem, 11vw, 3.2rem);
		}

		.about-copy {
			font-size: 1rem;
		}
	}
</style>
