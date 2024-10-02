<script>
	export let items = ["opcion1", "opcion2", "opcion3", "opcion4", "opcion5"];
	export let label = "Default label";
</script>

<div class="mb-3">
	<label for="exampleFormControlInput1" class="form-label">{label}</label>
	<select class="form-select" aria-label="Default select example">
		<option selected>--seleccionar--</option>
		{#each items as item}
			<option>One</option>
		{/each}
	</select>
</div>
