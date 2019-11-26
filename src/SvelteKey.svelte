<script>
	export let key
	// we just need a 1-length array
	const items = [0]
</script>

{#each items as x (key)}
	<slot />
{/each}
