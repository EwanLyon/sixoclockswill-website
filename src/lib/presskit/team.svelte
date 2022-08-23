<script lang="ts">
	export let name: string;
	export let role: string;
</script>

<div>
	<h4>{name}</h4>
	<span>{role}</span>
</div>

<style>
	h4 {
		font-family: 'Boogaloo';
		margin: 0.5em 0 0 0;
	}
</style>