<script>
    import { onMount } from 'svelte';

    onMount(() => {
        console.log("Home page loaded");
    });
</script>

<div id="background">
<h1>Contact Us</h1>
<div id="info">
<p id="contact">Contact Us through: <br>
Email: websitehelp@help.com <br>
Phone: +353 1 123 456 7890 <br> <br>
Visit our FAQ page for commonly asked questions:</p>
<p id="link">link</p>
</div>
</div>

<style>
    h1 { color: #00c721; }
    #contact { font-size: 18px;
               color: black;
               padding-top: 5%; }
    #info { margin-left: 10%;
            margin-right: 10%;
            margin-bottom: 5%;
            background-color: rgba(214, 223, 167, 0.7); 
            border-radius: 25px; 
            border-style:dotted;
            border-color: #00c721; 
            height: 600px;
        align-content: center; }
    #background { background-image: url('$lib/img/greenLeaf.jpg');
                  background-size:300%;
                  background-repeat: no-repeat;
                  padding-top: 1%;
                  padding-bottom: 1%;
                  margin-bottom: 70px;
                  border-radius: 25px;
                  height: 750px; }
    #link { text-decoration: underline;
            color: blue;
            padding-bottom: 5%; }
</style>