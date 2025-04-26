
<script>
    // @ts-nocheck
    
        import { onMount } from "svelte";
      
        // Fält för att mata in födelsedatum
        let birthDay = 0;
        let birthMonth = 0;
        let birthYear = 0;
      
        /*
         @type {string | any[]}
         */
        let results = [];
        let errorMessage = "";
    
        onMount(() => {
            console.log('the component has mounted');
        });
      
        // Lista med beräkningar
        const calculations = [
          { name: "Dagar levt", formula: (/** @type {number} */ ms) => Math.floor(ms / (1000 * 60 * 60 * 24)) },
          { name: "Timmar levt", formula: (/** @type {number} */ ms) => Math.floor(ms / (1000 * 60 * 60)) },
          { name: "Minuter levt", formula: (/** @type {number} */ ms) => Math.floor(ms / (1000 * 60)) },
          { name: "Sekunder levt", formula: (/** @type {number} */ ms) => Math.floor(ms / 1000) }
        ];
      
        function calculate() {
            console.log("Calculating!")
          errorMessage = "";
          results = [];
      
          // Kontrollera att alla fält är ifyllda
          if (birthDay <= 0 || birthMonth <= 0 || birthYear <= 0) {
         errorMessage = "Fill in all fields correctly!";
         return;
        }
      
          // Skapa ett datumobjekt från inmatningen
          let birthDate = new Date(birthYear, birthMonth - 1, birthDay);
      
          // Kontrollera att datumet är giltigt
          if (isNaN(birthDate.getTime())) {
            errorMessage = "Invalid date, please check your input.";
            return;
          }
      
          let now = new Date();
          // @ts-ignore
          let timeLived = now - birthDate;
      
          // Kontrollera att födelsedatumet inte är i framtiden
          if (timeLived < 0) {
            errorMessage = "The date cannot be in the future!";
            return;
          }
      
          // Beräkna värden baserat på tid i millisekunder
          results = calculations.map(calc => ({
            name: calc.name,
            value: calc.formula(timeLived).toLocaleString() // Formaterar siffror snyggt
          }));
        }

    
      </script>




<main class="grid grid-cols-[30%_40%_30%] grid-rows-[10%_10%_10%_5%_5%_10%_40%]">

    <div class="rubrik col-start-2 row-start-2 justify-self-center"><h1>LIFESTATS</h1></div>
    
    <div id="type" class="col-start-2 row-start-4 row-end-7 justify-self-center w-139 h-12"> Your birthdate:</div>

    <div id="day" class="col-start-2 row-start-5 justify-self-start m-3">         
        <input class="bibi w-25" type="number" placeholder="Day" min="1" max="31"
        on:input={(e) => birthDay = +e.target.value}>   
    </div>

    <div id="month" class="col-start-2 row-start-5 justify-self-center m-3">         
        <input class="bibi w-25" type="number" placeholder="Month" min="1" max="12"
        on:input={(e) => birthMonth = +e.target.value}>    
    </div>

    <div id="year" class="col-start-2 row-start-5 justify-self-end m-3">         
        <input class="bibi w-25" type="number" placeholder="Year" min="1900" max="2025"
        on:input={(e) => birthYear = +e.target.value}>    
    </div>
   
    <div id="calculate" class="col-start-2 row-start-6 justify-self-center m-15">
        <button class="button" on:click={() => { console.log("Klickade på knappen!"); calculate(); }}>
            Calculate
          </button>
          
    </div>

    <div id="bild" class="col-start-2 row-start-7">
        <img src="/earth.png" alt="earth">
    </div>
    
    <div class="fixed bottom-30 justify-self-center">
       {#if errorMessage}
            <p class="error">{errorMessage}</p>
        {/if}
    
        {#if results.length > 0}
            <ul class="result">
                {#each results as result}
                    <li>{result.name}: <strong>{result.value}</strong></li>
                 {/each}
            </ul>
        {/if}
    </div>
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
        background-color: rgb(6, 10, 17);
    }

    #bild {
        /* display: flex;
        justify-content: center; */
        opacity: 0;
    }

    #result {
        height: 100%;
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
        color:#ffffff;
        background-color: rgb(69, 84, 114);
        font-size: 20pt;
        /* border: 2px solid rgb(69, 84, 114); */
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .button {
        width: 555px;
    }

    .result {
        color: white;
    }

</style>

















