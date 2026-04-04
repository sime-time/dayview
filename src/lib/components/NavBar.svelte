<script lang="ts">
import logo from "$lib/assets/dayview.webp";

let menuOpen = $state(false);

const navLinks = [
	{ href: "/", label: "home" },
	{ href: "/#portfolio", label: "portfolio" },
	{ href: "/#about", label: "about" },
];

const closeMenu = () => {
	menuOpen = false;
};
</script>

<header class="navbar-wrap">
	<nav class="navbar" aria-label="Main navigation">
		<a class="brand" href="/" aria-label="Go to home section" onclick={closeMenu}>
			<img src={logo} alt="Dayanna logo" />
		</a>

		<ul class="nav-links desktop-links">
			{#each navLinks as link}
				<li>
					<a href={link.href}>{link.label}</a>
				</li>
			{/each}
		</ul>

		<a class="cta desktop-cta" href="/contact">contact me</a>

		<button
			type="button"
			class="menu-toggle"
			onclick={() => (menuOpen = !menuOpen)}
			aria-expanded={menuOpen}
			aria-controls="mobile-menu"
		>
			<span>{menuOpen ? 'Close' : 'Menu'}</span>
		</button>
	</nav>

	{#if menuOpen}
		<div class="mobile-menu" id="mobile-menu">
			<ul class="nav-links mobile-links">
				{#each navLinks as link}
					<li>
						<a href={link.href} onclick={closeMenu}>{link.label}</a>
					</li>
				{/each}
			</ul>
			<a class="cta mobile-cta" href="/contact" onclick={closeMenu}>contact me</a>
		</div>
	{/if}
</header>

<style>
	.navbar-wrap {
		position: sticky;
		top: 0;
		z-index: 200;
		padding: 0.9rem 1rem;
		background: linear-gradient(to bottom, rgb(255 255 255 / 0.92), rgb(255 255 255 / 0.76));
		backdrop-filter: blur(24px);
	}

	.navbar {
		max-width: 1180px;
		margin: 0 auto;
		display: grid;
		grid-template-columns: auto 1fr auto;
		align-items: center;
		gap: 1rem;
		padding: 0.4rem 1rem;
	}

	.brand {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		border-radius: 9999px;
	}

	.brand img {
		display: block;
		width: 96px;
		height: 96px;
		object-fit: contain;
	}

	.nav-links {
		list-style: none;
		margin: 0;
		padding: 0;
		display: flex;
		align-items: center;
		gap: 2.15rem;
	}

	.nav-links a {
		font-family: var(--font-sans);
		font-size: 1rem;
		font-weight: 600;
		letter-spacing: 0.01em;
		color: var(--color-text);
		transition: color 180ms ease;
	}

	.nav-links a:hover {
		color: var(--color-accent);
	}

	.desktop-links {
		justify-self: center;
	}

	.cta {
		display: inline-flex;
		align-items: center;
		justify-content: center;
		padding: 0.82rem 1.8rem;
		border-radius: 9999px;
		background: var(--color-primary);
		font-family: var(--font-sans);
		font-size: 0.98rem;
		font-weight: 700;
		letter-spacing: 0.01em;
		color: #ffffff;
		box-shadow: var(--shadow-ambient);
		transition: background-color 180ms ease, transform 180ms ease;
	}

	.cta:hover {
		background: var(--color-accent);
		transform: translateY(-1px);
	}

	.menu-toggle {
		display: none;
		align-items: center;
		justify-content: center;
		padding: 0.65rem 1rem;
		border: 0;
		border-radius: 9999px;
		background: var(--color-primary);
		color: #ffffff;
		font-family: var(--font-sans);
		font-size: 0.88rem;
		font-weight: 700;
		letter-spacing: 0.08em;
		text-transform: uppercase;
		cursor: pointer;
	}

	.mobile-menu {
		max-width: 1180px;
		margin: 0.35rem auto 0;
		padding: 1rem;
		border-radius: 24px;
		background: rgb(255 255 255 / 0.84);
		backdrop-filter: blur(24px);
		box-shadow: var(--shadow-ambient);
	}

	.mobile-links {
		flex-direction: column;
		align-items: flex-start;
		gap: 1rem;
		margin-bottom: 1.15rem;
	}

	.mobile-cta {
		width: 100%;
	}

	@media (max-width: 900px) {
		.navbar-wrap {
			padding: 0.7rem 0.6rem;
		}

		.navbar {
			grid-template-columns: 1fr auto;
		}

		.brand {
			justify-self: start;
			margin-left: -0.3rem;
		}

		.brand img {
			width: 90px;
			height: 90px;
		}

		.desktop-links,
		.desktop-cta {
			display: none;
		}

		.menu-toggle {
			display: inline-flex;
		}
	}
</style>
