<script>
	import { onNavigate } from '$app/navigation';
	import { ModeWatcher, toggleMode } from 'mode-watcher';
	import Switch from '$lib/components/ui/switch/switch.svelte';
	import imt from '$lib/images/logo imt.png'
	import '../app.css';
	import Footer from './Footer.svelte';
	import { onMount } from 'svelte';
	import { page } from '$app/stores';
	import { currentPage } from './shared.svelte';
	let { children } = $props();

	onMount(() => {
		let url = $page.url.pathname.substring(1);
		if (url === "") {
			currentPage.pageCount = 0
		} else if (url === "finish") {
			currentPage.pageCount = 6
		} else if (!isNaN(parseInt(url))) {
			currentPage.pageCount = parseInt(url)
		} else {
			currentPage.pageCount = 0
		}
	})

	onNavigate((navigation) => {
		if (!document.startViewTransition) return;

		return new Promise((resolve) => {
			document.startViewTransition(async () => {
				resolve();
				await navigation.complete;
			})
		})
	})
</script>

<ModeWatcher track={false} defaultMode={"light"}/>

<div class="app flex h-screen flex-col">
	<header class="flex m-3">
		<div class="corner">
			<img src={imt} alt='Logo IMT "Signum" ITB'>
		</div>
		<div class="corner p-3">
			<Switch on:click={toggleMode}/>
		</div>
	</header>
	<hr class="h-0.5 border-t-0 bg-neutral-100 dark:bg-white/10" />

	<main class="flex-1">		
		{@render children()}
	</main>

	<Footer />
</div>

<style>

	header {
		height: 4em;
		justify-content: space-between;

	}
	.corner {
		width: 3m;
		height: 3em;
	}

	.corner img {
		width: 3em;
		height: 3em;
		/* object-fit: contain; */
	}
</style>