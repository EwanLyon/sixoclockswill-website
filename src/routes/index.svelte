<script lang="ts">
	import { onMount } from 'svelte';

	let Carousel: any; // for saving Carousel component class
	let carousel: { goToNext: () => void }; // for calling methods of the carousel instance
	onMount(async () => {
		// @ts-ignore
		const module = await import('svelte-carousel');
		Carousel = module.default;
		console.log(Carousel);
	});

	const gameplayImages = [
		'/media/gameplay/WhiteWine.png',
		'/media/gameplay/RumAndTonic.png',
		'/media/gameplay/BarBible.png',
		'/media/gameplay/Beer.png',
		'/media/gameplay/VodkaTonic.png',
		'/media/gameplay/MainMenu.png',
	];
</script>

<svelte:head>
	<title>Six O'clock Swill</title>
	<meta content="Six O'clock Swill" property="og:title" />
	<meta content="The website for the Six O'clock Swill game!" property="og:description" />
</svelte:head>

<p id="tag-line">Get ready. The Six O'clock Swill is about to begin.</p>

<video id="hero-video" controls autoplay muted loop src="/media/SixOclockSwillAttractComp.mp4" />

<p>
	Play as a bartender in 1950s Melbourne trying to serve drinks and please customers. See how long
	you can serve customers as the stakes continually rise.
</p>

<p><a href="https://liquor-license-required.itch.io/six-oclock-swill" target="_blank" rel="noopener noreferrer"
	>itch.io Page</a
></p>

<svelte:component this={Carousel} let:loaded bind:this={carousel} autoplay autoplayDuration={6000}>
	{#each gameplayImages as src, imageIndex (src)}
		<div class="img-container">
			{#if loaded.includes(imageIndex)}
				<img {src} alt="Gameplay of Six O'clock Swill" />
			{/if}
		</div>
	{/each}
</svelte:component>

<h3>We will be at PAX Aus!</h3>
<p id="pax-desc">Come check out the game at the Swinburne booth (Booth 1440).</p>
<p>The game will be released at the end of the year.</p>

<style>
	#tag-line {
		margin-top: 0.5rem;
	}

	#hero-video {
		width: 70vw;
		margin: 2em;
		margin-top: 0;
		height: auto;
		border: 5px solid black;
	}

	h3 {
		font-family: 'Boogaloo';
		margin-bottom: 0;
	}

	.img-container {
		display: block;
		width: 100%;
	}

	.img-container > img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		-webkit-user-drag: none;
	}

	#pax-desc {
		margin: 0;
	}

	p {
		text-align: center;
	}

	/* Phone */
	@media (max-width: 992px) {
		#hero-video {
			width: 90vw;
		}
	}
</style>
