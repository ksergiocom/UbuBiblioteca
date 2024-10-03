<script>
	import Input from "$lib/components/Input.svelte";
	import Select from "$lib/components/Select.svelte";
	import Button from "$lib/components/Button.svelte";
</script>

<p class="lead">Aquí iría texto para explicar que es lo que se hace en cada sección, ayudas para guiar al usuario, etc.</p>
<form action="/inventario">
	<Input label="Nombre"/>
	<Input label="ISBN"/>
	<Input label="Cantidad"/>
	<Select label="Sala"/>
	<Button>Crear</Button>
</form>

