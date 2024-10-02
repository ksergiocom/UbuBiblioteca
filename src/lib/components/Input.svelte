<script>
	export let label = "Label"
	export let placeholder
</script>

<div class="mb-3">
	<label for="exampleFormControlInput1" class="form-label"
		>{label}</label
	>
	<input
		type="email"
		class="form-control"
		id="exampleFormControlInput1"
		{placeholder}
	/>
</div>
