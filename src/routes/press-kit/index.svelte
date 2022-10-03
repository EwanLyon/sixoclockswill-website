<script lang="ts">
	import TeamData from '$lib/team.json';
</script>

<svelte:head>
	<title>Press Kit - Six O'clock Swill</title>
	<meta content="Press Kit - Six O'clock Swill" property="og:title" />
</svelte:head>

<img id="hero-image" src="/media/GameLogo.png" alt="Six O'clock Swill logo" />
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
				<a href="https://sixoclockswill.net/" target="_blank" rel="noopener noreferrer"
					>SixOclockSwill.net</a
				>
			</p>
		</section>
		<section>
			<h3>Development Start</h3>
			<p>March, 2022</p>
		</section>
		<section>
			<h3>Platforms</h3>
			<p>PC, Mac</p>
		</section>
		<section>
			<h3>Socials</h3>
			<p>
				Twitter <a href="https://twitter.com/6oclockSwill" target="_blank" rel="noopener noreferrer"
					>@6oclockSwill</a
				>
			</p>
		</section>
		<section>
			<h3>Distribution</h3>
			<p>
				<a
					href="https://liquor-license-required.itch.io/six-oclock-swill"
					target="_blank"
					rel="noopener noreferrer">itch.io</a
				>
			</p>
		</section>
	</aside>
	<article id="description">
		<section>
			<h2>About</h2>
			<p>
				Six O'clock Swill is a physics based bartender simulator based in 1950s Melbourne. Attempt
				to serve drinks to ever increasing demanding customers since your reputation is on the line.
			</p>
			<p>
				Work during the daytime making cocktails and pouring spirits as best you can. When 5 o'clock
				hits all that goes out the window! A mass of people have arrived since finishing their day
				at work and now want a drink before the bar closes at 6! Work as fast as you can with an
				endless amount of people yearning for a pint before you close.
			</p>
		</section>
		<section>
			<h3>History</h3>
			<h4>Six O'clock Swill</h4>
			<p>
				The Six O'clock Swill is time in Australian and New Zealand history where between 1916–1960s
				there were restricted bar trading hours as as a rush of people buying drinks at bars after
				work at 5pm and before bars closed at 6pm. This led to mass drinking after 5pm when people
				got off work to drink as much as one could before the bar closed at 6pm. Bars compensated by
				making longer bars and tiling walls and floors to make them easier to clean. The 6pm closing
				time was extended to different times in different states between the late 1930s to late
				1960s. <a
					href="https://en.wikipedia.org/wiki/Six_o%27clock_swill"
					target="_blank"
					rel="noopener noreferrer">Six O'clock Swill Wikipedia page.</a
				>
			</p>
			<h4>John Brack</h4>
			<p>
				John Brack (1920–1999) was an Australian painter who often painted life and the people of
				Melbourne. One of his most notable paintings is <em>Collins St. 5pm</em> (1955) which
				depicts a mass of people leaving their work at 5pm heading home or towards the pub. We took
				heavy inspiration off this piece when an early prototype reminded our playtesters of the
				iconic art piece. The bar name in game is called "Bracks" in honour of John Brack. The
				artwork is currently being displayed at the NGV.
				<a href="https://en.wikipedia.org/wiki/John_Brack" target="_blank" rel="noopener noreferrer"
					>John Brack's Wikipedia page</a
				>.
				<a
					href="https://www.ngv.vic.gov.au/explore/collection/work/3161/"
					target="_blank"
					rel="noopener noreferrer"><em>Collins St, 5pm</em> NGV.</a
				>
			</p>
		</section>
		<section>
			<h3>Team</h3>
			<p>
				Six O'clock Swill was developed by Liquor License Required. A team forming of Swinburne
				University students for their capstone games project. The team comprises of 3 Designers /
				Programmers, 1 dedicated Programmer, 3 Artists, 1 Sound Designer and music composed by an
				artist from Polytech Melbourne. To find out more about the team check out the <a
					href="/team">team page!</a
				>
			</p>
		</section>
	</article>
</div>

<div id="media">
	<h2>Videos</h2>
	<video src="/media/SixOclockSwillAttractComp.mp4" controls>
		<track kind="captions" />
	</video>
	<h2>Images</h2>
	<a href="/media/sixoclockswill-images.zip" target="_blank" rel="noopener noreferrer"
		>Link to download all images</a
	>
	<section id="images">
		<img src="/media/gameplay/WhiteWine.png" alt="Six O'clock Swill Gameplay, pouring a white wine" />
		<img src="/media/gameplay/RumAndTonic.png" alt="Six O'clock Swill Gameplay, making a rum and tonic" />
		<img src="/media/gameplay/BarBible.png" alt="Six O'clock Swill Gameplay, showing the bar bible" />
		<img src="/media/gameplay/Beer.png" alt="Six O'clock Swill Gameplay, pouring a beer" />
		<img src="/media/gameplay/VodkaTonic.png" alt="Six O'clock Swill Gameplay, making a vodka tonic" />
		<img src="/media/gameplay/MainMenu.png" alt="Six O'clock Swill's Main Menu" />
	</section>
	<h2>Logos</h2>
	<a href="/media/Gameplay01.png" target="_blank" rel="noopener noreferrer"
		>Link to download logos</a
	>
	<section id="images">
		<img src="/media/GameLogo.png" alt="Six O'clock Swill Logo Square" />
		<img src="/media/GameLogoHorizontal.png" alt="Six O'clock Swill Logo Horizontal" />
		<img src="/media/TeamLogo.png" alt="Liquor License Required Logo" />
		<img src="/media/TeamLogoWhite.png" alt="Liquor License Required Logo White" class="dark" />
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
			<a href="https://twitter.com/6oclockSwill" target="_blank" rel="noopener noreferrer"
				>@6oclockSwill</a
			>
		</p>
		<h3>Email</h3>
		<p>
			<a href="mailto:sixoclockswillgame@gmail.com">sixoclockswillgame@gmail.com</a>
		</p>
		<h3>Website</h3>
		<p>
			<a href="https://sixoclockswill.net/" target="_blank" rel="noopener noreferrer"
				>SixOclockSwill.net</a
			>
		</p>
		<h3>itch.io</h3>
		<p>
			<a
				href="https://liquor-license-required.itch.io/six-oclock-swill"
				target="_blank"
				rel="noopener noreferrer">Six O'clock Swill</a
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

	#factsheet p,
	#contact p {
		margin: 0;
	}

	#press-kit,
	#media,
	#footer {
		font-size: 0.6em;
	}

	#hero-image {
		margin: 1em;
		max-width: 20vh;
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
		grid-template-columns: repeat(2, 50%);
		gap: 1em;
		justify-content: center;
		align-items: center;
	}

	#images img {
		width: 100%;
		height: auto;
		object-fit: contain;
		max-height: 25vh;
	}

	#images .dark {
		background: #000000;
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

	@media (max-width: 768px) {
		#hero-image {
			width: 100vw;
			height: auto;
		}

		#footer,
		#images,
		#press-kit {
			grid-template-columns: 100%;
		}

		#contact {
			text-align: left;
			padding: 0;
		}

		video {
			width: 100%;
		}
	}
</style>
