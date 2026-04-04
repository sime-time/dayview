<script lang="ts">
import logo from "$lib/assets/dayview.png";
</script>

<footer class="footer" aria-label="Site footer">
	<div class="footer-inner">
		<div class="brand-wrap">
			<img src={logo} alt="Dayview logo" />
		</div>

		<nav class="socials" aria-label="Social media links">
			<a href="https://instagram.com" target="_blank" rel="noreferrer" aria-label="Open Instagram">Instagram</a>
			<a href="https://tiktok.com" target="_blank" rel="noreferrer" aria-label="Open TikTok">TikTok</a>
		</nav>

		<p class="copyright">© 2026 Dayview. All rights reserved.</p>
	</div>
</footer>

<style>
	.footer {
		padding: clamp(2rem, 4.5vw, 3.2rem) 1rem;
		background: var(--color-accent-soft);
	}

	.footer-inner {
		max-width: 980px;
		margin: 0 auto;
		display: grid;
		grid-template-columns: 1fr auto;
		grid-template-areas:
			'brand socials'
			'copyright socials';
		align-items: center;
		column-gap: clamp(1.4rem, 3vw, 3rem);
		row-gap: 0.7rem;
	}

	.brand-wrap img {
		display: block;
		width: 176px;
		height: 176px;
		object-fit: contain;
		margin: 0 auto;
	}

	.brand-wrap {
		grid-area: brand;
		justify-self: start;
		margin-bottom: -0.2rem;
	}

	.socials {
		grid-area: socials;
		display: flex;
		align-items: center;
		justify-content: flex-end;
		gap: clamp(1.8rem, 4vw, 4.5rem);
	}

	.socials a {
		position: relative;
		font-family: var(--font-sans);
		font-size: clamp(0.92rem, 1.5vw, 1.12rem);
		font-weight: 700;
		letter-spacing: 0.085em;
		text-transform: uppercase;
		color: var(--color-text);
		transition: color 180ms ease;
	}

	.socials a::after {
		content: '';
		position: absolute;
		left: 0;
		right: 0;
		bottom: -0.28rem;
		height: 2px;
		background: var(--color-accent);
		transform: scaleX(0);
		transform-origin: center;
		transition: transform 180ms ease;
	}

	.socials a:hover {
		color: var(--color-accent);
	}

	.socials a:hover::after {
		transform: scaleX(1);
	}

	.copyright {
		grid-area: copyright;
		justify-self: start;
		margin: 0;
		font-family: var(--font-sans);
		font-size: clamp(0.73rem, 1.1vw, 0.9rem);
		font-weight: 600;
		letter-spacing: 0.06em;
		text-transform: uppercase;
		color: var(--color-muted);
		opacity: 0.85;
	}

	@media (max-width: 680px) {
		.footer-inner {
			display: flex;
			flex-direction: column;
			align-items: center;
			text-align: center;
			gap: clamp(1.1rem, 2.2vw, 1.8rem);
		}

		.footer {
			padding-top: 1.7rem;
			padding-bottom: 2rem;
			padding-inline: 0.65rem;
		}

		.brand-wrap,
		.copyright {
			justify-self: center;
		}

		.socials {
			justify-content: center;
		}

		.brand-wrap img {
			width: 138px;
			height: 138px;
		}

		.socials {
			gap: 1.5rem;
		}
	}
</style>
