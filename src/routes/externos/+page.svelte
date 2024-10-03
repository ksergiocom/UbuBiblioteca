<script>
	let pagina = "internos"
</script>

<h1>Externos</h1>


<ul class="nav nav-tabs mt-4">
	<li class="nav-item">
		<a
			class="nav-link"
			class:active={pagina == "internos"}
			on:click={() => (pagina = "internos")}>Internos</a
		>
	</li>
	<li class="nav-item">
		<a
			class="nav-link"
			class:active={pagina == "externos"}
			on:click={() => (pagina = "externos")}>Externos</a
		>
	</li>
</ul>


{#if pagina == 'internos'}
	<table class="table">
		<thead>
			<tr>
				<th>Recurso</th>
				<th>Visibilidad</th>
			</tr>
		</thead>
		<tbody>
			{#each Array.from(Array(10).keys()) as num}
			<tr>
				<td>Recurso{num}</td>
				<td>
					<div class="form-check form-switch">
					<input class="form-check-input" type="checkbox" role="switch" id="flexSwitchCheckDefault" checked={Math.random()>0.5?true:false}>
				  </div>
				</td>
			</tr>
			{/each}
		</tbody>
	</table>
	{:else}
	<table class="table">
		<thead>
			<tr>
				<th>Recurso</th>
				<th></th>
			</tr>
		</thead>
		<tbody>
			{#each Array.from(Array(4).keys()) as num}
			<tr>
				<td>API externa {num}</td>
				<td>
					<a
					href="/externos"
					class="btn btn-sm btn-primary"
					><i class="bi bi-pen"></i></a
				>
				<a
				href="/externos"
				class="btn btn-sm btn-danger"
				><i class="bi bi-trash"></i></a
			>
				</td>
			</tr>
			{/each}
		</tbody>
	</table>
{/if}