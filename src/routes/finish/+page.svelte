<script>

	import { fade } from "svelte/transition";
    import Button from "$lib/components/ui/button/button.svelte";
    import { currentPage } from "../shared.svelte";

</script>
<div class="h-full content-center justify-center" transition:fade>
    <h1 class="mb-4 text-4xl font-extrabold leading-none tracking-tight dark:text-white text-center">
        Terima Kasih!
    </h1>
    <h1 class="text-center dark:text-white">Ditunggu chapter selanjutnya 😊</h1>
    <div class="flex justify-center my-10">
        <Button href="/" onclick={() => {currentPage.pageCount=0}}>Home</Button>
    </div>
</div>

<style>
    
</style>