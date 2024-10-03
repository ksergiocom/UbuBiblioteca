<script>
	let computers = [
	  { id: 1, user: "User 1", timeLeft: "30 min" },
	  { id: 2, user: "User 2", timeLeft: "45 min" },
	  { id: 3, user: "User 3", timeLeft: "15 min" },
	  { id: 4, user: null, timeLeft: null }, // Puesto sin asignar
	  { id: 5, user: "User 4", timeLeft: "20 min" },
	  { id: 7, user: null, timeLeft: null }, // Puesto sin asignar
	  { id: 8, user: null, timeLeft: null }, // Puesto sin asignar
	  { id: 9, user: null, timeLeft: null }, // Puesto sin asignar
	  { id: 10, user: null, timeLeft: null }, // Puesto sin asignar
	  { id: 11, user: null, timeLeft: null }, // Puesto sin asignar
	  { id: 12, user: null, timeLeft: null }, // Puesto sin asignar
	  { id: 13, user: null, timeLeft: null }, // Puesto sin asignar

	];
  </script>
  
  <style>
	.grid-container {
	  display: grid;
	  grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
	  gap: 1rem;
	}
  
	.card-body ul {
	  padding-left: 0;
	  list-style: none;
	}
  
	.card {
	  min-width: 150px;
	  max-width: 150px;
	}
  
  </style>
  
  <h1 class="mb-3">Listado de computadores</h1>
  <div class="grid-container">
	{#each computers as computer}
	  <div class="card">
		<div class="card-header">
		  <h5 class="card-title">#{computer.id}</h5>
		</div>
		<div class="card-body">
		  <ul>
			{#if computer.user}
			  <li><strong>Usuario:</strong> {computer.user}</li>
			  <li><strong>Tiempo:</strong> {computer.timeLeft}</li>
			{:else}
			  <li class="text-secondary">Puesto sin asignar</li>
			{/if}
		  </ul>
		  {#if computer.user}
		  <div class="d-flex gap-1">


			<button class="btn btn-secondary btn-sm">Ajustar</button>
		  <button class="btn btn-danger btn-sm">Retirar</button>
		</div>
			{:else}
			<button class="btn btn-primary btn-sm">Asignar</button>
		  {/if}

		</div>
	  </div>
	{/each}
  </div>
  