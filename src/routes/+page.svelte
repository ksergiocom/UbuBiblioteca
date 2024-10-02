<script>
	import Input from '$lib/components/Input.svelte'
	import Button from '$lib/components/Button.svelte'
</script>

<form action="/inventario">
	<Input label="Usuario"/>
	<Input label="Contraseña"/>
	<Button>Iniciar sesión</Button>
</form>
