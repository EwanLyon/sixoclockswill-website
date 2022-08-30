<script>
	import TeamMember from '$lib/team/TeamMember.svelte';

	import EwanImg from './Ewan.png';
	import ChrisImg from './Chris.jpg';
	import RyanCImg from './RyanC.jpg';
	import Placeholder01Img from './Placeholder01.jpg';
	import Placeholder02Img from './Placeholder02.jpg';
	import Placeholder03Img from './Placeholder03.jpg';
	import Placeholder04Img from './Placeholder04.jpg';
</script>

<section>
	<h1>The Team</h1>
	<p class="nowrap">
		We are a group of students working on this game during 2022 at the Swinburne University of
		Technology.
	</p>

	<div class="team-grid">
		<TeamMember name="Ewan Lyon" image={EwanImg} description="Programmer / Designer" social="https://twitter.com/Clubwhom" />
		<TeamMember name="Ryan Chessum" image={RyanCImg} description="Programmer / Designer" />
		<TeamMember name="Chris Wiltshire" image={ChrisImg} description="Programmer / Designer" />
		<TeamMember name="Ryan Sharp" image={Placeholder01Img} description="Programmer" />
		<TeamMember name="Adam Kelsey" image={Placeholder02Img} description="Artist" />
		<TeamMember name="Sayankumar Chandara Sagar" image={Placeholder03Img} description="Artist" />
		<TeamMember name="Alec Stewart" image={Placeholder01Img} description="Artist" />
		<TeamMember name="Dan Chadderton" image={Placeholder04Img} description="Sound Designer" />
	</div>
</section>

<style>
	h1 {
		font-family: 'Boogaloo';
		text-align: center;
	}

	p {
		text-align: center;
	}

	.team-grid {
		display: grid;
		/* width: 120%; */
		gap: 1em 2em;
		grid-auto-rows: 1fr;
		grid-template-columns: 25% 25% 25% 25%;
		justify-content: center;
	}

	/* Desktop */
	@media (min-width: 992px) {
		.nowrap {
			white-space: nowrap;
		}
	}

	/* Phone */
	@media (max-width: 768px) {
		.team-grid {
			grid-template-columns: 100%;
		}
	}

	/* Tablet */
	@media (min-width: 768px) and (max-width: 992px) {
		.team-grid {
			grid-template-columns: 50% 50%;
		}
	}
</style>
