<script>
	import Button from '$lib/components/Button.svelte'
</script>


<h1>Socios</h1>

<div class="d-flex gap-3">
	<Button href="/socios/form">Crear socio</Button>
	<Button href="/socios/form">Nuevo préstamo</Button>
</div>

<table class="table mt-4">
	<thead>
		<tr>
			<th>ID</th>
			<th>Socio</th>
			<th>Fecha</th>
			<th></th>
		</tr>
	</thead>
	<tbody>
		{#each Array.from(Array(20).keys()) as num}
		<tr>
			<td>ID</td>
			<td>Socio 1</td>
			<td>1999/01/01</td>
			<td>						<a
				href="/socios/form"
				class="btn btn-sm btn-primary"
				><i class="bi bi-pen"></i></a
			>
			<a
			href="/socios"
			class="btn btn-sm btn-danger"
			><i class="bi bi-trash"></i></a
		></td>
		</tr>
		{/each}
	</tbody>
  </table>