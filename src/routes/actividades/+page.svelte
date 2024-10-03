<script>
	import Button from "$lib/components/Button.svelte";
</script>

<h1>Actividades</h1>

<div class="d-flex">
	<Button className="my-3" href="/actividades/form">Crear actividad</Button>
</div>

<div id="carouselExample" class="carousel slide">
	<div class="carousel-inner">
		<div class="carousel-item active">
			<img
				src="https://picsum.photos/id/237/600/400"
				class="d-block w-100"
				alt="actividad1"
			/>
		</div>
		<div class="carousel-item">
			<img
				src="https://picsum.photos/id/238/600/400"
				class="d-block w-100"
				alt="actividad1"
			/>
		</div>
		<div class="carousel-item">
			<img
				src="https://picsum.photos/id/239/600/400"
				class="d-block w-100"
				alt="actividad1"
			/>
		</div>
	</div>
	<button
		class="carousel-control-prev"
		type="button"
		data-bs-target="#carouselExample"
		data-bs-slide="prev"
	>
		<span class="carousel-control-prev-icon" aria-hidden="true"></span>
		<span class="visually-hidden">Previous</span>
	</button>
	<button
		class="carousel-control-next"
		type="button"
		data-bs-target="#carouselExample"
		data-bs-slide="next"
	>
		<span class="carousel-control-next-icon" aria-hidden="true"></span>
		<span class="visually-hidden">Next</span>
	</button>
</div>

<table class="table mt-4">
	<thead>
		<tr>
			<th>Nombre</th>
			<th></th>
		</tr>
	</thead>
	<tbody>
		{#each Array.from(Array(20).keys()) as num}
			<tr>

				<td>Evento 1</td>

				<td>
					{#if Math.random()>0.5}
					<a href="/inventario/libro" class="btn btn-sm btn-success"
						><i class="bi bi-person"></i></a
					>
					{:else}
					<a href="/inventario/libro" class="btn btn-sm btn-outline-secondary"
					><i class="bi bi-person-slash"></i></a
				>
					{/if}
					{#if Math.random()>0.5}
					<a href="/inventario/libro" class="btn btn-sm btn-success"
						><i class="bi bi-send"></i></a
					>
					{:else}
					<a href="/inventario/libro" class="btn btn-sm btn-outline-secondary"
					><i class="bi bi-send-slash"></i></a
				>
					{/if}
					<a href="/inventario/libro" class="btn btn-sm btn-primary"
						><i class="bi bi-pen"></i></a
					>
					<a href="/inventario/libro" class="btn btn-sm btn-danger"
						><i class="bi bi-trash"></i></a
					></td
				>
			</tr>
		{/each}
	</tbody>
</table>
