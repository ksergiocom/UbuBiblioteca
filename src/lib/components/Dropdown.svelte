<script>
	export let items = []
</script>

<div class="dropdown">
	<button class="btn btn-primary dropdown-toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
		<slot></slot>
	</button>
	<ul class="dropdown-menu">
		{#each items as item}
			{#if item.title == 'divider'}
			<li><hr class="dropdown-divider"></li>
			{:else}
			<li><a class="dropdown-item" href="{item.href}">{item.title}</a></li>
			{/if}
		{/each}
	</ul>
  </div>