<script>
	import { page } from '$app/stores';

	let links = [
		{titulo:'Inventario',href:'/inventario'},
		{titulo:'Actividades',href:'/actividades'},
		{titulo:'Computadores',href:'/computadores'},
		{titulo:'Externos',href:'/externos'},
		{titulo:'Reportes',href:'/reportes'},
	]
</script>


<nav class="px-1 navbar navbar-expand-lg bg-body-tertiary" data-bs-theme="dark">
	<div class="container-fluid">
		<a class="navbar-brand" href="/">UbuBiblioteca</a>
		<button
			class="navbar-toggler"
			type="button"
			data-bs-toggle="collapse"
			data-bs-target="#navbarNavDropdown"
			aria-controls="navbarNavDropdown"
			aria-expanded="false"
			aria-label="Toggle navigation"
		>
			<span class="navbar-toggler-icon"></span>
		</button>
		<div class="collapse navbar-collapse" id="navbarNavDropdown">
			<ul class="navbar-nav">
				{#each links as link }
					<li class="nav-item">
						<a class="nav-link {$page.url.pathname.includes(link.href)?'active':''}" aria-current="page" href="{link.href}">{link.titulo}</a>
					</li>	
				{/each}
			</ul>
		</div>
	</div>
</nav>