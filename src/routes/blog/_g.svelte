<script>
    import { browser } from '$app/env'; 
    import mermaid from 'mermaid';
    import { onMount } from 'svelte';

    let graph = null;

    mermaid.initialize({
        startOnLoad: false,

        theme: 'forest'
    });

    onMount(() => {
        mermaid.init([ graph ]);
    });
</script>

<main>
    {#if browser}
    <pre bind:this={graph}>
			<slot />
    </pre>
    {/if}
</main>