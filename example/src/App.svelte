<script>
	import Identity from 'svelte-key'
	let i = 0
</script>

<p>Change input value & click button</p>

<Identity key={i}>
	<input />
</Identity>

<button on:click={() => {i++}}>
	{i}
</button>
