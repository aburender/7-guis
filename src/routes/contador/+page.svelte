<script lang="ts">
	let value = $state(0);

	function onclick() {
		value++;
	}
</script>

<fieldset role="group">
	<input type="number" bind:value readonly />
	<button {onclick}>Incrementar</button>
</fieldset>
