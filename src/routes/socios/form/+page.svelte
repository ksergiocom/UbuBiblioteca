<script>
	import Input from "$lib/components/Input.svelte";
	import Button from "$lib/components/Button.svelte";
</script>

<form action="/socios">
	<Input label="Nombre"/>
	<Input label="Fecha" type="date"/>
	<Input label="Contraseña" type="date"/>
	<div class="form-floating mb-4 mt-4">
		<textarea class="form-control" placeholder="Leave a comment here" id="floatingTextarea2" style="height: 200px"></textarea>
		<label for="floatingTextarea2">Descripción</label>
	  </div>
	<Button>Crear</Button>
</form>

