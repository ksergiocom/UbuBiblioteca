<script>
	import Input from "$lib/components/Input.svelte";
	import Select from "$lib/components/Select.svelte";
	import Button from "$lib/components/Button.svelte";
</script>

<form action="/inventario">
	<p class="lead">
		Aquí agregaríamos cosas para poder hacer consultas con más opciones. Esto se tendría que hacer sobre un recurso concreto para saber que opciones de consulta/filtrado habría.
	</p>
	<Input label="Nombre"/>
	<Input label="ISBN"/>
	<Select label="Fecha"/>
	<Select label="Sala"/>
	<div class="form-check mb-3 mt-4">
		<input class="form-check-input" type="radio" name="flexRadioDefault" id="flexRadioDefault1">
		<label class="form-check-label" for="flexRadioDefault1">
			Opcion 1
		</label>
	  </div>
	  <div class="form-check mb-3">
		<input class="form-check-input" type="radio" name="flexRadioDefault" id="flexRadioDefault2" checked>
		<label class="form-check-label" for="flexRadioDefault2">
		  Opcion 2
		</label>
	  </div>
	<Button className="mt-3">Buscar</Button>
</form>

