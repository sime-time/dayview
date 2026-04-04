<script lang="ts">
import dayanna from "$lib/assets/dayanna-dress.png";
</script>

<section class="hero" id="home" aria-label="Hero section">
	<div class="hero-inner">
		<header class="headline-wrap">
			<h1 class="headline-sans">Hi I'm Day</h1>
			<p class="headline-serif">Creative Director</p>
		</header>

		<p class="availability">
			<span class="dot" aria-hidden="true"></span>
			Available for new opportunities
		</p>

		<p class="hero-copy">Social media videographer for <u>event promotion</u> and <u>personal branding.</u></p>

		<div class="hero-image-wrap">
			<img src={dayanna} alt="Dayanna posing in a burgundy dress" />
		</div>

		<div class="hero-cta-wrap">
			<a href="#contact" class="hero-cta">Let's Talk</a>
		</div>
	</div>
</section>

<style>
	.hero {
		position: relative;
		overflow: clip;
		padding: clamp(1rem, 3vw, 2.2rem) 1rem 0;
		background: linear-gradient(to bottom, var(--color-surface) 0%, var(--color-accent) 100%);
	}

	.hero-inner {
		position: relative;
		z-index: 1;
		max-width: 1180px;
		margin: 0 auto;
		display: grid;
		grid-template-columns: minmax(0, 1fr) minmax(460px, 620px) minmax(0, 1fr);
		grid-template-rows: auto auto auto;
		align-items: start;
		gap: 0.5rem;
	}

	.availability {
		grid-column: 1;
		grid-row: 2;
		justify-self: start;
		align-self: center;
		display: inline-flex;
		align-items: center;
		gap: 0.6rem;
		margin: 0;
		padding: 0.62rem 1.06rem;
		border-radius: 9999px;
		background: rgb(255 255 255 / 0.9);
		backdrop-filter: blur(20px);
		box-shadow: var(--shadow-ambient);
		font-family: var(--font-sans);
		font-size: 0.89rem;
		font-weight: 600;
		color: var(--color-text);
	}

	.dot {
		width: 0.72rem;
		height: 0.72rem;
		border-radius: 50%;
		background: var(--color-accent);
		box-shadow: 0 0 0 6px rgb(255 102 196 / 0.18);
	}

	.headline-wrap {
		grid-column: 1 / 4;
		grid-row: 1;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 0;
		text-align: center;
		margin-top: -1.2rem;
		z-index: 1;
	}

	.headline-sans {
		margin: 0;
		font-family: var(--font-sans);
		font-size: clamp(2.1rem, 6.7vw, 5.8rem);
		line-height: 0.95;
		letter-spacing: -0.032em;
		font-weight: 430;
		color: var(--color-text);
	}

	.headline-serif {
		margin: 0;
		font-family: var(--font-serif);
		font-style: italic;
		font-size: clamp(2.6rem, 8.9vw, 7.7rem);
		line-height: 0.92;
		letter-spacing: -0.03em;
		font-weight: 400;
		color: var(--color-text);
	}

	.hero-copy {
		grid-column: 3;
		grid-row: 2;
		justify-self: end;
		text-align: right;
		align-self: center;
		max-width: 30ch;
		margin: -2.2rem 0 0;
		font-family: var(--font-sans);
		font-size: 1.1rem;
		line-height: 1.45;
		font-weight: 600;
		color: var(--color-text);
	}

	.hero-image-wrap {
		grid-column: 2;
		grid-row: 1 / 4;
		position: relative;
		z-index: 3;
		align-self: end;
		justify-self: center;
		width: min(100%, 620px);
		margin-top: 1.8rem;
	}

	.hero-image-wrap img {
		display: block;
		width: 100%;
		height: auto;
		object-fit: contain;
		filter: grayscale(1) contrast(1.06) brightness(1.03) drop-shadow(0 30px 55px rgb(17 17 17 / 0.16));
	}

	.hero-cta-wrap {
		grid-column: 3;
		grid-row: 3;
		justify-self: end;
		align-self: start;
		margin-top: 1rem;
		margin-bottom: 0;
	}

	.hero-cta {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		padding: 1rem 2.1rem;
		border-radius: 9999px;
		background: var(--color-primary);
		font-family: var(--font-sans);
		font-size: 1rem;
		font-weight: 700;
		letter-spacing: 0.01em;
		color: #ffffff;
		box-shadow: var(--shadow-ambient);
		transition: transform 180ms ease, background-color 180ms ease;
	}

	.hero-cta:hover {
		background: var(--color-accent);
		transform: translateY(-1px);
	}

	@media (max-width: 1100px) {
		.hero-inner {
			grid-template-columns: 1fr;
			grid-template-rows: auto;
			justify-items: center;
			gap: 0.85rem;
		}

		.headline-wrap,
		.availability,
		.hero-copy,
		.hero-image-wrap,
		.hero-cta-wrap {
			grid-column: 1;
			justify-self: center;
		}

		.headline-wrap {
			grid-row: 1;
			margin-top: 0;
			z-index: 2;
			transform: none;
		}

		.hero-image-wrap {
			grid-row: 2;
			width: min(88vw, 540px);
			margin-top: -0.3rem;
			z-index: 1;
			transform: none;
		}

		.availability {
			grid-row: 3;
		}

		.hero-copy {
			grid-row: 4;
			max-width: 34ch;
			margin: 0;
			text-align: center;
			font-size: 1rem;
		}

		.hero-cta-wrap {
			grid-row: 5;
			margin-top: 0.55rem;
			margin-bottom: 0.45rem;
		}
	}

	@media (min-width: 1101px) {
		.hero {
			min-height: calc(100vh - 96px);
		}

		.headline-wrap {
			transform: translateY(-24px);
		}

		.hero-image-wrap {
			transform: translateY(42px);
		}
	}

	@media (max-width: 640px) {
		.hero {
			padding-top: 0.8rem;
		}

		.headline-wrap {
			gap: 0;
		}

		.headline-sans {
			font-size: clamp(2rem, 13vw, 3.5rem);
		}

		.headline-serif {
			font-size: clamp(2.4rem, 15.5vw, 4.25rem);
		}

		.availability {
			font-size: 0.84rem;
			padding: 0.58rem 0.9rem;
		}

		.hero-image-wrap {
			width: min(90vw, 420px);
		}

		.hero-cta {
			padding-inline: 1.8rem;
		}
	}
</style>
