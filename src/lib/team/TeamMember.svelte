<script lang="ts">
	export let name: string;
	export let description: string;
	export let image: string;
	export let social: string | undefined = undefined;
</script>

<div class="team-member">
	<img src={image} alt={`Photo of ${name}`} />
	<span>{name}</span>
	{#if social}
		<p><a href={social} target="_blank" rel="noopener noreferrer">{description}</a></p>
	{:else}
		<p>{description}</p>
	{/if}
</div>

<style>
	.team-member {
		width: 100%;
		max-width: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		text-align: center;
	}

	img {
		width: 75%;
		border: 2px solid black;
		margin-bottom: 0.25em;
	}

	.team-member span {
		font-family: 'Boogaloo';
		font-size: 1.3em;
		/* font-weight: bold; */
		white-space: nowrap;
	}

	.team-member p {
		margin-top: 0.1em;
	}

	a {
		color: black;
	}

</style>
