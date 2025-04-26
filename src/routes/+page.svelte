
<script>

    let days = $state(0)

    let weeks = $derived(days / 7)

    let year = $derived(days / 365)

    let andetag = $derived(days * 25000)

    let hjärtslag = $derived(days * 100000)

    let jorden = $derived(days / 29.5)

    let blinka = $derived(days * 10000)

    let sova = $derived(days / 3)

</script>

<main class="grid grid-cols-[30%_40%_30%] grid-rows-[10%_10%_10%_10%_5%_5%_10%_30%_30%_30%_30%_30%_30%_30%_30%]">

    <div id="rubrik" class="rubrik col-start-2 row-start-2 justify-self-center"><h1>LIFESTATS</h1></div>
    
    <div id="type" class="col-start-2 row-start-5 row-end-5"> Hur många dagar är du? </div>
   
    <input id="skriv" class="col-start-2 row-start-6 row-end-6 h-[50px]" type="number" bind:value={days} />

    <section id="dagarlevt" class="col-start-1 col-end-4 row-start-8 row-end-8">
        <p>Du har levt {days} dagar</p>
    </section>

    <section id="veckorlevt" class="col-start-1 col-end-4 row-start-9 row-end-9">
        <p>Du har levt {weeks} veckor</p>
    </section>

    <section id="årlevt" class="col-start-1 col-end-4 row-start-10 row-end-10">
        <p>Du har levt {year} år</p>
    </section>

    <section id="årlevt" class="col-start-1 col-end-4 row-start-11 row-end-11">
        <p>Du har tagit {andetag} andetag</p>
    </section>

    <section id="hjärta" class="col-start-1 col-end-4 row-start-12 row-end-12">
        <p>Ditt hjärta har slått {hjärtslag} gånger</p>
    </section>

    <section id="jorden" class="col-start-1 col-end-4 row-start-13 row-end-13">
            <p>Månen har hunnit roterat {jorden} varv runt jorden under din livstid</p>
    </section>

    <section id="blinka" class="col-start-1 col-end-4 row-start-14 row-end-14">
        <p>Du har blinkat {blinka} gånger</p>
    </section>

    <section id="sova" class="col-start-1 col-end-4 row-start-15 row-end-15">
        <p>Du har sovit i {sova} dagar. Det är en tredjedel av ditt liv!</p>
    </section>

</main>


<style>

 @font-face {
    font-family: 'champagne';
    /* font-style: normal; */
    /* font-weight: 500; */
    /* src: url('../../static/Champagne.ttf') format('truetype'); */
 }
    main {
        /* background-color: rgb(121, 136, 164); */
        background-color: rgb(18, 28, 45);
        /* background-color: rgb(125, 153, 201); */
        height: 100vh;
    }

    #dagarlevt {
        /* background-color: #ffffff; */
        color:#ffffff;
        border: none;
        display: flex;
        justify-content: center;
    }

    #veckorlevt {
        background-color:rgb(18, 28, 45);
        color:#ffffff;
        border: none;
        display: flex;
        justify-content: center;
    }

    #årlevt {
        color:#ffffff;
        display: flex;
        justify-content: center;
        background-color: rgb(18, 28, 45);
    }

    #jorden {
        color:#ffffff;
        display: flex;
        justify-content: center;
        background-color: rgb(18, 28, 45);
    }

    #hjärta {
        color:#ffffff;
        display: flex;
        justify-content: center;
        background-color: rgb(18, 28, 45);
    }

    #blinka {
        color:#ffffff;
        display: flex;
        justify-content: center;
        background-color: rgb(18, 28, 45);
    }
    
    #sova {
        color:#ffffff;
        display: flex;
        justify-content: center;
        background-color: rgb(18, 28, 45);
    }

    #skriv {
        border: none;
        border: none;
        border: solid 1px rgb(18, 28, 45);
    }

    #bild {
        /* display: flex;
        justify-content: center; */
        opacity: 0;
    }

    h1 {
        /* display: flex;
        justify-content: center;
        align-items: center; */
        font-family: 'champagne';
        font-size: 70pt;
        color: #ffffff;
        /* padding: 50px; */
    }

    button {
      padding: 0.7rem 1.5rem;
      background-color: rgb(43, 56, 82);
      font-size: 20pt;
      color: white;
      border: none;
      border-radius: 0px;
      cursor: pointer;
    }

    button:hover {
      background-color: rgb(95, 112, 145);
    }

    .error {
      color: rgb(255, 196, 196);
      font-weight: bold;
      margin-top: 1rem;
    }

    #day input {
        background-color: rgb(95, 112, 145);
        color: #ffffff;
        border: none;
    }

    #month input {
        background-color: rgb(95, 112, 145);
        color: #ffffff;
        border: none;
    }

    #year input {
        background-color: rgb(95, 112, 145);
        color: #ffffff;
        border: none;
    }

    .bibi::placeholder {
        color: #ffffff;
    }

    #type {
        background-color:#ffffff;
        color: black;
        /* color: rgb(69, 84, 114); */
        /* font-size: 20pt; */
        /* border: 2px solid rgb(69, 84, 114); */
        border: solid 1px rgb(18, 28, 45);
        display: flex;
        align-items: center;
        padding-left: 10px;
    }

    .button {
        width: 555px;
    }

    .result {
        color: white;
    }

    #rubrik {
        font-family:Verdana, Geneva, Tahoma, sans-serif;
    }

</style>

















