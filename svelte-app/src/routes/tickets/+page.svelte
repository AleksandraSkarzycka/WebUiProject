<script>
    import { onMount } from 'svelte';
    import rollercoaster from '$lib/img/rollercoaster1.jpg';

    onMount(() => {
        console.log("Ticket page loaded");
    });

    let minPrice = 0;
    let maxPrice = 999;

    let passes = [
        {
        name: "Weekend Pass",
        price: 35,
        description: "Spend a chosen weekend at Chessington’s theme park to unwind! Includes entry to Theme Park & Zoo. Under 90cms visit free!",
        image: rollercoaster
        },
        {
        name: "1 Day Pass",
        price: 29,
        description: "Includes entry to Theme Park & Zoo. Save up to €37 when you book in advance. Under 90cms visit free!",
        image: rollercoaster
        },
        {
        name: "Chessington Annual Pass",
        price: 60,
        description: "Spend a day at the park! Includes entry to Theme Park & Zoo!",
        image: rollercoaster
        },
        {
        name: "Adult and Preschooler Pass",
        price: 30,
        description: "Includes entry to Theme Park and Zoo! Mid-week, term time only. Valid for 1 child aged 4 years or under any any accompanying adult. Under 90cms visit free!",
        image: rollercoaster
        },
        {
        name: "Adult and Preschooler Annual Pass",
        price: 55,
        description: "Mid-week term time entry to Chessington World of Adventures Resort*. 10% off in retail shops. 20% off food & beverage. Valid for 1 child aged 4 years or under any any accompanying adult.",
        image: rollercoaster
        },
        {
        name: "Overnight Stays",
        price: 32,
        description: "A Delicious Breakfast. Themed & Standard Rooms. Early Ride Access. Free Parking. Hotel Entertainment",
        image: rollercoaster
        },
        {
        name: "10-30 Groups",
        price: 32,
        description: "Book for your tribe to visit Britain’s Wildest Adventure this year! Discover magical rides and attractions and over 1000 animals in our ZOO and SEA LIFE Centre.",
        image: rollercoaster
        },
        {
        name: "31-100 Groups",
        price: 32,
        description: "Save when you come on a wild adventure to Chessington as a group of 31-100. With magical rides and attractions, plus our Zoo and SEA LIFE centre, there’s so much to explore.",
        image: rollercoaster
        },
        {
        name: "Exclusive Student Discount",
        price: 20,
        description: "Get discounted entry to Britain’s Wildest Adventure with Student Beans. Discover magical rides and attractions from Vampire and Dragon’s Fury to the jaw-dropping Croc Drop, there’s something for those daring or those looking for light thrills! Plus, don’t miss the chance to come face-to-face with over 1,000 animals and underwater creatures in our Zoo and SEA LIFE too.",
        image: rollercoaster
        }
    ];

    $: filteredPasses = passes.filter(pass =>
        pass.price >= minPrice && pass.price <= maxPrice
    );
</script>

<div id="background">

    <!-- Price Filter Controls -->
    <div id="filter">
        <label>Min Price:</label>
        <input type="number" bind:value={minPrice} min="0" />
        <label>Max Price:</label>
        <input type="number" bind:value={maxPrice} min="0" />
    </div>
    
    <div id="info">
        <!-- Card Display -->
        <div id="infocards">
            {#each filteredPasses as pass}
            <div class="card">
                <img src={pass.image} alt={pass.name} style="width:100%" />
                <h1>{pass.name}</h1>
                <p class="price">€{pass.price}</p>
                <p>{pass.description}</p>
                <p><button>Add to Cart</button></p>
            </div>
            {/each}
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
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

}

#info {
    margin-top: 1%;
    margin-left: 1%;
    margin-right: 1%;
    background-color: rgb(214, 223, 167, 0.7); 
    border-radius: 25px; 
    border-style:dotted;
    border-color: #00c721; 
    height:fit-content;
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

#infocards {
    display: flex;
    flex-wrap: wrap;
}

#filter {
    padding: 1%;
    background-color: rgb(214, 223, 167, 0.7);
    max-width:700px;
    border-radius: 25px;
}
</style>