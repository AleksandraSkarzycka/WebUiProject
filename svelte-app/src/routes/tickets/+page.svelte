<script>
    import { onMount } from 'svelte';
    import rollercoaster from '$lib/img/rollercoaster1.jpg';

    onMount(() => {
        console.log("Ticket page loaded");
    });
</script>

<div id="background">
<div id="info">
    <div class="card">
        <img src={rollercoaster} alt="Weekend Pass" style="width:100%">
        <h1>Weekend Pass</h1>
        <p class="price">€35</p>
        <p>Spend a chosen weekend at Chessington’s theme park to unwind!</p>
        <p><button>Add to Cart</button></p>
      </div>
      <div class="card">
        <img src={rollercoaster} alt="1 Day Pass" style="width:100%">
        <h1>1 Day Pass</h1>
        <p class="price">€29</p>
        <p>Spend a day at the park! <br>
           Includes entry to Theme Park & Zoo!</p>
        <p><button>Add to Cart</button></p>
      </div>
      <div class="card">
        <img src={rollercoaster} alt="Chessington Annual Pass" style="width:100%">
        <h1>Chessington Annual Pass</h1>
        <p class="price">€60</p>
        <p>Spend a day at the park! <br>
           Includes entry to Theme Park & Zoo!</p>
        <p><button>Add to Cart</button></p>
      </div>
</div>
</div>


<style>
#background { 
    background-image: url('$lib/img/greenLeaf.jpg');
    background-size:300%;
    background-repeat:no-repeat;
    padding-top: 1%;
    padding-bottom: 1%;
    margin-bottom: 70px;
    border-radius: 25px;
    height: fit-content;
}

#info {
    display: flex;
    margin-left: 1%;
    margin-right: 1%;
    background-color: rgb(214, 223, 167, 0.7); 
    border-radius: 25px; 
    border-style:dotted;
    border-color: #00c721; 
    height:fit-content;
    align-content: center;
}

.card {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    background-color: white;
    max-width: 300px;
    max-height: 100vh;
    margin: 1%;
    text-align: center;
    font-family: arial;
}

.price {
    color: grey;
    font-size: 22px;
}

.card button {
    border: none;
    outline: 0;
    padding: 12px;
    color: white;
    background-color: #000;
    text-align: center;
    cursor: pointer;
    width: 100%;
    font-size: 18px;
}

.card button:hover {
    opacity: 0.7;
}
</style>