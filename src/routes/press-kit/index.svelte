<script lang="ts">
	import TeamData from '$lib/team.json';
	import Logo from '$lib/header/logo.png';
</script>

<img id="hero-image" src={Logo} alt="Six O'clock Swill logo" />
<div id="press-kit">
	<aside id="factsheet">
		<h2>Factsheet</h2>
		<section>
			<h3>Developers</h3>
			<p>Liquor License Required</p>
		</section>
		<section>
			<h3>Location</h3>
			<p>Melbourne, Australia</p>
		</section>
		<section>
			<h3>Website</h3>
			<p>
				<a href="http://sixoclockswill.com.au/" target="_blank" rel="noopener noreferrer"
					>SixOclockSwill.com.au</a
				>
			</p>
		</section>
		<section>
			<h3>Development Start</h3>
			<p>March, 2022</p>
		</section>
		<section>
			<h3>Platform</h3>
			<p>PC, Mac</p>
		</section>
		<section>
			<h3>Socials</h3>
			<p>
				Twitter <a
					href="https://twitter.com/sixoclockswillgame"
					target="_blank"
					rel="noopener noreferrer">@SixOclockSwillGame</a
				>
			</p>
		</section>
	</aside>
	<article id="description">
		<section>
			<h2>About</h2>
			<p>Six O'clock Swill is a physics based bartender simulator based in 1950s Melbourne.</p>
		</section>
		<section>
			<h3>History</h3>
			<p>Six O'clock Swill is... TBA</p>
		</section>
	</article>
</div>

<div id="media">
	<h2>Videos</h2>
	<video src="/media/gameplay.webm" controls>
		<track kind="captions" />
	</video>
	<h2>Images</h2>
	<a href="/media/sixoclockswill-images.zip" target="_blank" rel="noopener noreferrer"
		>Link to download all images</a
	>
	<section id="images">
		<img src="/media/Gameplay01.png" alt="Gameplay" />
		<img src="/media/Gameplay02.png" alt="Gameplay" />
		<img src="/media/Gameplay03.png" alt="Gameplay" />
		<img src="/media/Gameplay04.png" alt="Gameplay" />
	</section>
	<h2>Logos</h2>
	<a href="/media/Gameplay01.png" target="_blank" rel="noopener noreferrer"
		>Link to download logos</a
	>
	<section id="images">
		<img src={Logo} alt="Logo" />
	</section>
</div>

<!-- <div id="articles">
	<h2>Articles</h2>
</div> -->

<div id="footer">
	<div id="team">
		<h2>Team</h2>
		{#each TeamData as Member}
			<div>
				<h3>{Member.name}</h3>
				{#if Member.social}
					<a href={Member.social} target="_blank" rel="noopener noreferrer">{Member.role}</a>
				{:else}
					<span>{Member.role}</span>
				{/if}
			</div>
		{/each}
	</div>
	<div id="contact">
		<h2>Contact</h2>
		<h3>Twitter</h3>
		<p>
			<a href="https://twitter.com/sixoclockswillgame" target="_blank" rel="noopener noreferrer"
				>@SixOclockSwillGame</a
			>
		</p>
		<h3>Tiktok</h3>
		<p>
			<a href="https://twitter.com/sixoclockswillgame" target="_blank" rel="noopener noreferrer"
				>@SixOclockSwillGame</a
			>
		</p>
		<h3>Website</h3>
		<p>
			<a href="http://sixoclockswill.com.au/" target="_blank" rel="noopener noreferrer"
				>SixOclockSwill.com.au</a
			>
		</p>
		<h3>Email</h3>
		<p>
			<a href="https://twitter.com/sioclockswill" target="_blank" rel="noopener noreferrer"
				>sixoclockswill@gmail.com</a
			>
		</p>
	</div>
</div>

<style>
	* {
		font-family: 'Noto Serif';
	}

	h2 {
		font-family: 'Roboto Slab';
	}

	h2 {
		margin-bottom: 0.2em;
	}

	h3 {
		margin: 0;
	}

	p {
		margin: 0;
	}

	#press-kit,
	#media,
	#footer {
		font-size: 0.6em;
	}

	#hero-image {
		margin: 1em;
	}

	#press-kit {
		display: grid;
		grid-template-columns: 1fr 2fr;
		gap: 2em;
		width: 80%;
	}

	#description section {
		margin-bottom: 0.75em;
	}

	#media {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	#media a {
		margin-bottom: 0.5em;
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

	#factsheet section {
		margin-bottom: 0.5em;
	}

	#footer {
		display: grid;
		grid-template-columns: 1fr 2fr;
		width: 80%;
	}

	#team h3 {
		margin-top: 0.5em;
		gap: 2em;
	}

	#team a {
		color: black;
	}

	#contact {
		/* text-align: right; */
		padding: 0 1em;
		text-align: right;
	}

	#contact h3 {
		margin-top: 0.5em;
	}
</style>
