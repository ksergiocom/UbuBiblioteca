<h1>Detalle de un socio</h1>

<table class="table mt-4">
	<thead>
		<tr>
			<th>Libro</th>
			<th>Fecha prestamo</th>
			<th>Fecha Vencimiento</th>
			<th></th>
		</tr>
	</thead>
	<tbody>
		{#each Array.from(Array(20).keys()) as num}
			<tr>
				<td>Libro{num}</td>
				<td>1999/01/01</td>
				<td>2020/01/01</td>
				<td>
					<a href="/socios/form" class="btn btn-sm btn-primary"
						><i class="bi bi-pen"></i></a
					>
					{#if Math.random() > 0.5}
						<a href="/socios" class="btn btn-sm btn-success"
							><i class="bi bi-check"></i></a
						>
					{:else}<a href="/socios" class="btn btn-sm btn-outline-success"
							><i class="bi bi-x"></i></a
						>{/if}
				</td>
			</tr>
		{/each}
	</tbody>
</table>
