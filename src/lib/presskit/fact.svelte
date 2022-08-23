<script lang="ts">
	export let title: string;
	export let fact: string;
	export let link: string | undefined = undefined;
</script>

<section>
	<h3>{title}</h3>
	{#if link}
		<a href={link} target="_blank" rel="noreferrer">{fact}</a>
	{:else}
		<p>{fact}</p>
	{/if}
</section>

<style>
	section {
		margin-bottom: 0.5em;
	}

	h3 {
		font-family: 'Boogaloo';
		margin: 0;
	}

	p {
		margin: 0;
	}
</style>
