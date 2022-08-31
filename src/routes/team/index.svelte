<script>
	import TeamData from '$lib/team.json';
	import TeamMember from '$lib/team/TeamMember.svelte';
</script>

<svelte:head>
	<title>The Team - Six O'clock Swill</title>
	<meta content="The Team - Six O'clock Swill" property="og:title" />
	<meta content="The team behind Six O'clock Swill" property="og:description" />
</svelte:head>

<section>
	<h1>The Team</h1>
	<p class="nowrap">
		We are a group of students working on this game during 2022 at the Swinburne University of
		Technology.
	</p>

	<div class="team-grid">
		{#each TeamData as Member}
			<TeamMember name={Member.name} image={Member.image} description={Member.role} social={Member.social} />
		{/each}
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
