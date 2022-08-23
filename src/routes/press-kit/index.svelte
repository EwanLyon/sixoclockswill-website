<script lang="ts">
	import Fact from '$lib/presskit/fact.svelte';
	import Team from '$lib/presskit/team.svelte';

	import TeamData from '$lib/team.json';
	import Logo from '$lib/header/logo.png';
</script>

<img id="hero-image" src={Logo} alt="Six O'clock Swill logo" />
<div id="press-kit">
	<aside id="factsheet">
		<h2>Factsheet</h2>
		<Fact title="Developer" fact="Liquor License Required" />
		<Fact title="Location" fact="Melbourne, Australia" />
		<Fact title="Website" fact="sixoclockswill.com.au" link="https://sixoclockswill.com.au/" />
		<Fact title="Development Start" fact="March 22, 2022" />
		<Fact title="Platform" fact="PC" />
		<Fact title="Socials" fact="Twitter @SixOclockSwill" link="twitter.com/sioclockswill" />
	</aside>
	<article id="description">
		<section>
			<h2>About</h2>
			<p>Six O'clock Swill is a physics based bar tender simulation.</p>
		</section>
		<section>
			<h3>History</h3>
			<p>Six O'clock Swill is .</p>
		</section>
	</article>
</div>

<div id="media">
	<h2>Videos</h2>
	<video src="/media/gameplay.webm" controls >
		<track kind="captions" />
	</video>
	<h2>Images</h2>
	<section id="images">
		<img src="/media/Gameplay01.png" alt="Gameplay" />
		<img src="/media/Gameplay02.png" alt="Gameplay" />
		<img src="/media/Gameplay03.png" alt="Gameplay" />
		<img src="/media/Gameplay04.png" alt="Gameplay" />
	</section>
</div>

<!-- <div id="articles">
	<h2>Articles</h2>
</div> -->

<div id="team">
	<h2>Team</h2>
	{#each TeamData as Member}
		<Team name={Member.name} role={Member.role} />
	{/each}
</div>

<style>
	h2,
	h3 {
		font-family: 'Boogaloo';
	}

	h2 {
		margin-bottom: 0.2em;
	}

	h3 {
		margin-bottom: 0;
	}

	p {
		margin: 0;
	}

	#hero-image {
		margin: 1em;
	}

	#press-kit {
		display: grid;
		grid-template-columns: 30% auto;
		gap: 2em;
	}

	#media {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	video {
		width: 80%;
		height: auto;
	}

	#images {
		display: grid;
		grid-template-columns: 40% 40%;
		gap: 1em;
		justify-content: center;
	}

	#images img {
		width: 100%;
		height: auto;
	}
</style>
