<script>
	let pagina = "prestamos";
</script>

<h1>Reportes</h1>

<ul class="nav nav-tabs mt-4">
	<li class="nav-item">
		<a
			class="nav-link"
			class:active={pagina == "prestamos"}
			on:click={() => (pagina = "prestamos")}>Préstamos</a
		>
	</li>
	<li class="nav-item">
		<a
			class="nav-link"
			class:active={pagina == "actividades"}
			on:click={() => (pagina = "actividades")}>Actividades</a
		>
	</li>
	<li class="nav-item">
		<a
			class="nav-link"
			class:active={pagina == "catalogo"}
			on:click={() => (pagina = "catalogo")}>Catálogo</a
		>
	</li>
</ul>


<table class="table">
	{#if pagina=='prestamos'}
	<thead>
		<tr>
			<th>Nombre</th>
			<th></th>
		</tr>
	</thead>
	<tbody>
		{#each [1,2] as i}
			<tr>
				<td>Dato{i}</td>
				<td>
											<a
							href="/reportes/detalle"
							class="btn btn-sm btn-primary"
							><i class="bi bi-eye"></i></a
						>
				</td>
			</tr>
		{/each}
	</tbody>
	{:else if pagina=='actividades'}
	<thead>
		<tr>
			<th>Nombre</th>
			<th></th>
		</tr>
	</thead>
	<tbody>
		{#each [1,2] as i}
			<tr>
				<td>Dato{i}</td>
				<td>
											<a
							href="/reportes/detalle"
							class="btn btn-sm btn-primary"
							><i class="bi bi-eye"></i></a
						>
				</td>
			</tr>
		{/each}
	</tbody>
	{:else if pagina=='catalogo'}
	<thead>
		<tr>
			<th>Nombre</th>
			<th></th>
		</tr>
	</thead>
	<tbody>
		{#each [1,2] as i}
			<tr>
				<td>Dato{i}</td>
				<td>
											<a
							href="/reportes/detalle"
							class="btn btn-sm btn-primary"
							><i class="bi bi-eye"></i></a
						>
				</td>
			</tr>
		{/each}
	</tbody>
	{/if}

</table>