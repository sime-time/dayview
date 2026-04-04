<section class="contact" id="contact" aria-label="Contact section">
	<div class="contact-inner">
		<p class="eyebrow">Let's Collaborate</p>
		<h2>Ready to make your content impossible to ignore?</h2>
		<p class="subtext">
			Fill out a quick form and book a meeting with Dayanna to plan your next shortform video
			strategy.
		</p>
		<a href="/contact" class="cta" type="button" aria-label="Open booking form">Book a Meeting</a>
	</div>
</section>

<style>
	.contact {
		padding: clamp(3rem, 7vw, 6.2rem) 1rem clamp(4rem, 8vw, 7rem);
		background: var(--color-surface);
	}

	.contact-inner {
		max-width: 960px;
		margin: 0 auto;
		padding: clamp(2rem, 5vw, 4rem) clamp(1.1rem, 4vw, 3rem);
		border-radius: 30px;
		background: var(--color-surface-low);
		text-align: center;
	}

	.eyebrow {
		margin: 0 0 0.8rem;
		font-family: var(--font-sans);
		font-size: 0.72rem;
		font-weight: 700;
		letter-spacing: 0.16em;
		text-transform: uppercase;
		color: var(--color-accent);
	}

	h2 {
		margin: 0;
		font-family: var(--font-serif);
		font-style: italic;
		font-size: clamp(2rem, 5.6vw, 4rem);
		line-height: 0.95;
		letter-spacing: -0.02em;
		font-weight: 500;
		color: var(--color-text);
	}

	.subtext {
		margin: 1.2rem auto 0;
		max-width: 48ch;
		font-family: var(--font-sans);
		font-size: 1.05rem;
		line-height: 1.65;
		font-weight: 600;
		color: var(--color-muted);
	}

	.cta {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		margin-top: 1.9rem;
		padding: 0.96rem 2rem;
		border: 0;
		cursor: pointer;
		border-radius: 9999px;
		background: var(--color-primary);
		color: #ffffff;
		font-family: var(--font-sans);
		font-size: 0.98rem;
		font-weight: 700;
		letter-spacing: 0.01em;
		transition: background-color 180ms ease, transform 180ms ease;
	}

	.cta:hover {
		background: var(--color-accent);
		transform: translateY(-1px);
	}

	@media (max-width: 680px) {
		.contact {
			padding-inline: 0.65rem;
		}

		.subtext {
			font-size: 1rem;
		}
	}
</style>
