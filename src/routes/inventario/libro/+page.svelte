<script>
	import Input from "$lib/components/Input.svelte";
	import Select from "$lib/components/Select.svelte";
	import Button from "$lib/components/Button.svelte";
</script>

<form action="/inventario">
	<Input label="Nombre"/>
	<Input label="ISBN"/>
	<Input label="Cantidad"/>
	<Select label="Sala"/>
	<Button>Crear</Button>
</form>

