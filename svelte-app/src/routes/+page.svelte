<script>
    import { onMount } from 'svelte';

    onMount(() => {
        console.log("Home page loaded");
    });
</script>

<h1>Web UI Project</h1>
<p>Tickets page is dynamic <br>
About and Contact are static</p>

<style>
    h1 { color: #00c721; }
    p { font-size: 18px; }
</style>