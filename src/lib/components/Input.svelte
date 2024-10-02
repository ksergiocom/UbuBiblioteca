<script>
	export let label = "Label"
	export let placeholder
	export let type = "text"
</script>

<div class="mb-3">
	<label for="exampleFormControlInput1" class="form-label"
		>{label}</label
	>
	<input
		type="{type}"
		class="form-control"
		id="exampleFormControlInput1"
		{placeholder}
	/>
</div>
