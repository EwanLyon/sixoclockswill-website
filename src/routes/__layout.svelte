<script lang="ts">
	import Header from '$lib/header/Header.svelte';
</script>

<Header />

<main>
	<slot />
</main>

<footer>
	<p>© 2022 Liquor License Required</p>
</footer>

<style>
	@font-face {
		font-family: 'Shadows Into Light';
		font-style: normal;
		font-weight: 400;
		src: url('/media/ShadowsIntoLight-Regular.ttf') format('truetype');
	}

	@font-face {
		font-family: 'Boogaloo';
		font-style: normal;
		font-weight: 400;
		src: url('/media/Boogaloo-Regular.ttf') format('truetype');
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		/* width: 100%; */
		max-width: 1200px;
		margin: 0 auto;
		box-sizing: border-box;
		font-family: 'Shadows Into Light';
		font-size: 1.8rem;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
		font-family: 'Boogaloo';
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style>
