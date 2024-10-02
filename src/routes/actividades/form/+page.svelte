<script>
	import Input from "$lib/components/Input.svelte";
	import Select from "$lib/components/Select.svelte";
	import Button from "$lib/components/Button.svelte";
</script>

<form action="/actividades">
	<Input label="Nombre"/>
	<Input label="Fecha" type="date"/>
	<Select label="Sala"/>
	<div class="form-floating mb-4">
		<textarea class="form-control" placeholder="Leave a comment here" id="floatingTextarea2" style="height: 200px"></textarea>
		<label for="floatingTextarea2">Descripción</label>
	  </div>

	<Button href="/actividades/form">Crear</Button>
</form>

