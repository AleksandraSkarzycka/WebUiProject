<script>
    import { onMount } from 'svelte';

    onMount(() => {
        console.log("Ticket page loaded");
    });
</script>

<div id="background">

</div>


<style>
#background { background-image: url('$lib/img/greenLeaf.jpg');
                  background-size:cover;
                  background-repeat: no-repeat;
                  padding-top: 1%;
                  padding-bottom: 1%;
                  margin-bottom: 70px;
                  border-radius: 25px; }
</style>