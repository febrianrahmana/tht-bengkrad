<script>
    import Progress from "$lib/components/ui/progress/progress.svelte";
    import { currentPage } from "./shared.svelte";
    import Button from "$lib/components/ui/button/button.svelte";
    import { goto } from "$app/navigation";

    function previous() {
        currentPage.pageCount -= 1
        goto("/" + (currentPage.pageCount === 0 ? "" : currentPage.pageCount))
    }
    function next() {
        currentPage.pageCount += 1
        goto("/" + (currentPage.pageCount === 6 ? "finish" : currentPage.pageCount))
    }

    let progressValue = $derived(currentPage.pageCount*20)
</script>

<footer>
    <div class="flex justify-between">
        {#if currentPage.pageCount === 0}
        <Button disabled>
            <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
                <path fill="currentColor" d="M20 9v6h-8v4.84L4.16 12L12 4.16V9z" />
            </svg>
        </Button>
        {:else}
        <Button onclick={() => previous()}>
            <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
                <path fill="currentColor" d="M20 9v6h-8v4.84L4.16 12L12 4.16V9z" />
            </svg>
        </Button>
        {/if}
        {#if currentPage.pageCount === 6}
        <Button disabled>
            <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
                <path fill="currentColor" d="M4 15V9h8V4.16L19.84 12L12 19.84V15z" />
            </svg>
        </Button>
        {:else}
        <Button onclick={() => next()}>
            <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
                <path fill="currentColor" d="M4 15V9h8V4.16L19.84 12L12 19.84V15z" />
            </svg>
        </Button>
        {/if}
    </div>
    <div>
        <Progress value={progressValue} />
    </div>
</footer>