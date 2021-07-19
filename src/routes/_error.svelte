<script>
	import {onMount} from 'svelte'

	onMount(()=>{
		if ('serviceWorker' in navigator) navigator.serviceWorker.register('/service-worker.js'); 
		var s = document.createElement("script"); 
		try { new Function("if(0)import('')")(); s.src = "/client/client.f10c3e42.js"; s.type = "module"; s.crossOrigin = "use-credentials"; }
		catch (e) { s.src = "/client/shimport@1.0.1.js"; s.setAttribute("data-main", "/client/client.f10c3e42.js") }
		document.head.appendChild(s);
	})
	
</script>


<style>
	h1 {
		margin: 20% 0 !important;
		text-align: center;
		font-size: 2.8em;
		font-weight: 700;
		font-size: 2em;
	}
	main.svelte-tdnk6b {
		position: relative;
		box-sizing: border-box;
	}
	@keyframes svelte-1arwlvc-navani {
		0% {
			opacity: 0
		}

		100% {
			opacity: 1
		}
	}
</style>

<svelte:head>
	<title>404 or Offline</title>
</svelte:head>

<div id="sapper">
	<main class="svelte-tdnk6b">
		<h1 class="svelte-8od9u6">404 or Offline</h1>
	</main>
</div>

