<script lang="ts">
	import { page } from '$app/stores';
	import logo from './logo.png';
</script>

<header>
	<img src={logo} alt="Six O'clock Swill" />

	<nav>
		<ul>
			<li class:active={$page.url.pathname === '/'}><a sveltekit:prefetch href="/">Home</a></li>
			<li class:active={$page.url.pathname === '/team'}>
				<a sveltekit:prefetch href="/team">The Team</a>
			</li>
		</ul>
	</nav>
</header>

<style>
	header {
		display: flex;
		flex-direction: column;
		align-items: center;

		border-bottom: 5px solid black;
		padding: 0.75em;
	}

	img {
		width: auto;
		height: 5rem;
	}

	nav ul {
		display: flex;
		justify-content: center;
		gap: 2rem;
		/* font-family: 'Shadows Into Light'; */
		font-family: 'Boogaloo';
		font-size: 2em;
		margin-top: 0.3em;
		margin-bottom: 0;
	}

	li {
		list-style: none;
	}

	li.active {
		font-weight: bold;
	}

	a {
		color: black;
		text-decoration: none;
		transition: 0.2s;
	}

	a:hover {
		color: rgb(167, 167, 167);
	}
</style>
