<script>
	import { goto } from '$app/navigation';

	export let block = true
	export let href
	export let className = []
	
	function handleNavigation() {
		if(!href){
			return
		}

		goto(href);
	}
</script>

<button type="submit" class="btn btn-primary {block?'w-100':''} {className}" on:click={handleNavigation}>
	<slot>Aceptar</slot>
</button>