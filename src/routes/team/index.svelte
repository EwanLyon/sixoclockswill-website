<script>
	import TeamMember from '$lib/team/TeamMember.svelte';

	import EwanImg from './Ewan.png';
	import ChrisImg from './Chris.jpg';
	import RyanCImg from './RyanC.jpg';
</script>

<section>
	<h1>The Team</h1>
	<p class="nowrap">
		We are a group of students working on this game during 2022 at the Swinburne University of
		Technology.
	</p>

	<div class="team-grid">
		<TeamMember name="Ewan Lyon" image={EwanImg} description="Programmer / Designer" />
		<TeamMember name="Ryan Chessum" image={RyanCImg} description="Programmer / Designer" />
		<TeamMember name="Chris Wiltshire" image={ChrisImg} description="Programmer / Designer" />
		<TeamMember name="Ryan Sharp" image={EwanImg} description="Programmer" />
		<TeamMember name="Adam Kelsey" image={EwanImg} description="Artist" />
		<TeamMember name="Sayankumar Chandara Sagar" image={EwanImg} description="Artist" />
		<TeamMember name="Alec Stewart" image={EwanImg} description="Artist" />
		<TeamMember name="Dan Chadderton" image={EwanImg} description="Sound Designer" />
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
