<script>
	import Dropdown from "$lib/components/Dropdown.svelte";
	import Button from "$lib/components/Button.svelte";

	let items = [
		{ title: "Libro", href: "inventario/libro" },
		{ title: "Revista", href: "inventario/libro" },
		{ title: "Periódico", href: "inventario/libro" },
		{ title: "Recursos digitales", href: "inventario/libro" },
		{ title: "Coleccion especial", href: "inventario/libro" },
		{ title: "divider" },
		{ title: "Sala", href: "inventario/sala" },
	];

	let pagina = "catalogo";
</script>

<h1 class="mb-3">Inventario</h1>

<div class="d-flex items-center gap-3">
	<Dropdown {items}>Crear nuevo</Dropdown>
	<Button block={false} href="/inventario/avanzada">Consulta avanzada</Button>
</div>

<ul class="nav nav-tabs mt-4">
	<li class="nav-item">
		<a
			class="nav-link"
			class:active={pagina == "catalogo"}
			on:click={() => (pagina = "catalogo")}>Catálogo</a
		>
	</li>
	<li class="nav-item">
		<a
			class="nav-link"
			class:active={pagina == "sala"}
			on:click={() => (pagina = "sala")}>Salas</a
		>
	</li>
</ul>

{#if pagina == "catalogo"}
	<table class="table mt-3">
		<thead>
			<tr>
				<th>ISBN</th>
				<th>Titulo</th>
				<th>Cantidad</th>
				<th></th>
			</tr>
		</thead>
		<tbody>
			{#each Array.from(Array(10).keys()) as num}
				<tr>
					<td>{num}</td>
					<td>Libro{num}</td>
					<td>33/69</td>
					<td>
						<a
							href="/inventario/libro"
							class="btn btn-sm btn-primary"
							><i class="bi bi-pen"></i></a
						>
					</td>
				</tr>
			{/each}
		</tbody>
	</table>
{:else}
	<table class="table mt-3">
		<thead>
			<tr>
				<th>Sala</th>
				<th></th>
			</tr>
		</thead>
		<tbody>
			{#each Array.from(Array(10).keys()) as num}
				<tr>
					<td>Sala - {num}</td>
					<td>
						<a
							href="/inventario/sala"
							class="btn btn-sm btn-primary"
							><i class="bi bi-pen"></i></a
						>
					</td>
				</tr>
			{/each}
		</tbody>
	</table>
{/if}
