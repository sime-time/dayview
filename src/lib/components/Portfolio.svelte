<script lang="ts">
const reels = [
	{
		title: "oktoberfest",
		tag: "Event Promotion",
		placeholder: "placeholder-a",
	},
	{
		title: "villa lifestyle",
		tag: "Personal Branding",
		placeholder: "placeholder-b",
	},
	{
		title: "halloweenie",
		tag: "Event Promotion",
		placeholder: "placeholder-c",
	},
	{
		title: "cartel vibes",
		tag: "Personal Branding",
		placeholder: "placeholder-d",
	},
];
</script>

<section class="portfolio" id="portfolio" aria-label="Portfolio section">
	<div class="portfolio-inner">
		<div class="portfolio-head">
			<div>
				<p class="eyebrow">Selected Works</p>
				<h2>portfolio</h2>
			</div>
			<p class="intro">capturing motion, emotion, and the digital pulse of modern storytelling.</p>
		</div>

		<div class="reels-grid">
			{#each reels as reel}
				<article class="reel-card">
					<div class={`media ${reel.placeholder}`} aria-hidden="true"></div>
					<p class="tag">{reel.tag}</p>
					<h3>{reel.title}</h3>
				</article>
			{/each}
		</div>
	</div>
</section>

<style>
	.portfolio {
		padding: 0 1rem clamp(3.2rem, 6vw, 5rem);
		background: linear-gradient(to bottom, var(--color-accent) 0%, #ff8fd4 100%);
	}

	.portfolio-inner {
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
		font-style: italic;
		font-size: clamp(2.2rem, 6.5vw, 5.3rem);
		line-height: 0.9;
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

	.reels-grid {
		display: grid;
		grid-template-columns: repeat(4, minmax(0, 1fr));
		gap: clamp(1rem, 2vw, 1.7rem);
	}

	.reel-card {
		display: flex;
		flex-direction: column;
	}

	.media {
		aspect-ratio: 9 / 16;
		width: 100%;
		border-radius: 26px;
		margin-bottom: 0.95rem;
		box-shadow: 0 30px 58px rgb(17 17 17 / 0.08);
	}

	.placeholder-a {
		background:
			linear-gradient(180deg, rgb(255 255 255 / 0.12), rgb(38 9 26 / 0.5)),
			radial-gradient(circle at 52% 83%, #f43467 0%, #d70f50 34%, #4f1838 72%);
	}

	.placeholder-b {
		background:
			linear-gradient(180deg, rgb(255 255 255 / 0.1), rgb(14 8 35 / 0.6)),
			radial-gradient(circle at 48% 25%, #5963d9 0%, #2a185e 44%, #12081f 78%);
	}

	.placeholder-c {
		background:
			linear-gradient(180deg, rgb(255 255 255 / 0.08), rgb(26 10 1 / 0.56)),
			radial-gradient(circle at 60% 38%, #ef9054 0%, #a44b20 43%, #3b1808 79%);
	}

	.placeholder-d {
		background:
			linear-gradient(180deg, rgb(255 255 255 / 0.16), rgb(12 20 34 / 0.58)),
			radial-gradient(circle at 12% 20%, #4da7c0 0%, #236187 28%, #162438 72%);
	}

	.tag {
		align-self: flex-start;
		margin: 0 0 0.52rem;
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

	h3 {
		margin: 0;
		font-family: var(--font-sans);
		font-size: clamp(1.5rem, 2.1vw, 2.1rem);
		line-height: 1.1;
		letter-spacing: -0.015em;
		font-weight: 700;
		color: var(--color-text);
	}

	@media (max-width: 1080px) {
		.portfolio-head {
			grid-template-columns: 1fr;
			align-items: start;
		}

		.reels-grid {
			grid-template-columns: repeat(2, minmax(0, 1fr));
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

		.reels-grid {
			grid-template-columns: 1fr;
			gap: 1.35rem;
		}

		.media {
			max-width: 360px;
		}

		h3 {
			font-size: 1.9rem;
		}

		h2 {
			font-size: clamp(3.25rem, 14vw, 4.1rem);
			font-weight: 400;
			line-height: 0.88;
		}
	}
</style>
