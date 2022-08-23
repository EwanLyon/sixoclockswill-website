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
		src: url('/media/fonts/ShadowsIntoLight-Regular.ttf') format('truetype');
	}

	@font-face {
		font-family: 'Boogaloo';
		font-style: normal;
		font-weight: 400;
		src: url('/media/fonts/Boogaloo-Regular.ttf') format('truetype');
	}

	@font-face {
		font-family: 'Roboto Slab';
		font-style: normal;
		src: url('/media/fonts/RobotoSlab-VariableFont_wght.ttf') format('truetype');
	}

	@font-face {
		font-family: 'Noto Serif';
		font-style: normal;
		font-weight: 400;
		src: url('/media/fonts/NotoSerif-Regular.ttf') format('truetype');
	}

	@font-face {
		font-family: 'Noto Serif';
		font-style: italic;
		font-weight: 400;
		src: url('/media/fonts/NotoSerif-Italic.ttf') format('truetype');
	}

	@font-face {
		font-family: 'Noto Serif';
		font-style: normal;
		font-weight: 700;
		src: url('/media/fonts/NotoSerif-Bold.ttf') format('truetype');
	}

	@font-face {
		font-family: 'Noto Serif';
		font-style: italic;
		font-weight: 700;
		src: url('/media/fonts/NotoSerif-BoldItalic.ttf') format('truetype');
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
