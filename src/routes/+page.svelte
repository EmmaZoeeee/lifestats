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


<main class="grid grid-cols-[30%_40%_30%] grid-rows-[10%_10%_10%_10%_5%_5%_40%_100%_100%_100%_100%_100%_100%_20%_20%]">


   <section id="bildbakgrund" class="col-start-1 col-end-4 row-start-1 row-end-6">
       <img src="/Life stats bakgrund.png" alt="bakgrund">
   </section>


   <section id="bildbaby" class="col-start-1 col-end-4 row-start-6 row-end-7">
       <img src="/baby.png" alt="baby">
   </section>
 
 
   <div id="rubrik" class="rubrik col-start-2 row-start-2 justify-self-center"><h1>LIFESTATS</h1></div>
  
   <div id="type" class="col-start-2 row-start-5 row-end-5"> Hur många dagar är du? </div>
 
   <input id="skriv" class="col-start-2 row-start-6 row-end-6 h-[50px]" type="number" bind:value={days} />






   <section id="bildtid" class="col-start-1 col-end-4 row-start-8 row-end-8">
       <img src="/Life stats tid.png" alt="tid">
   </section>


   <section id="bildandas" class="col-start-1 col-end-4 row-start-9 row-end-9">
       <img src="/Life stats andas.png" alt="andas">
   </section>


   <section id="bildhjarta" class="col-start-1 col-end-4 row-start-10 row-end-10">
       <img src="/Life stats hjarta.png" alt="hjarta">
   </section>


   <section id="bildmanen" class="col-start-1 col-end-4 row-start-11 row-end-11">
       <img src="/Life stats manen.png" alt="manen">
   </section>


   <section id="bildblinka" class="col-start-1 col-end-4 row-start-12 row-end-12">
       <img src="/Life stats blinka.png" alt="blinka">
   </section>


   <section id="bildsova" class="col-start-1 col-end-4 row-start-13 row-end-13">
       <img src="/Life stats sova.png" alt="sova">
   </section>


   <section id="bildbakgrund2" class="col-start-1 col-end-4 row-start-14 row-end-15">
       <img src="/Life stats bakgrund2.png" alt="bakgrund">
   </section>










   <section id="dagarlevt" class="col-start-1 col-end-4 row-start-8 row-end-8">
       <p>Du har levt {days} dagar</p>
   </section>


   <section id="veckorlevt" class="col-start-1 col-end-4 row-start-8 row-end-8">
       <p>Det är {weeks} veckor</p>
   </section>


   <section id="årlevt" class="col-start-1 col-end-4 row-start-8 row-end-8">
       <p>Och {year} år</p>
   </section>


   <section id="andas" class="col-start-1 col-end-4 row-start-9 row-end-9">
       <p>Du har tagit {andetag} andetag</p>
   </section>


   <section id="hjärta" class="col-start-1 col-end-4 row-start-10 row-end-10">
       <p>Ditt hjärta har slagit {hjärtslag} gånger</p>
   </section>


   <section id="jorden" class="col-start-1 col-end-4 row-start-11 row-end-11">
           <p>Månen har hunnit roterat</p>
   </section>


   <section id="jorden2" class="col-start-1 col-end-4 row-start-11 row-end-11">
       <p>{jorden}</p>
   </section>


   <section id="jorden3" class="col-start-1 col-end-4 row-start-11 row-end-11">
       <p>varv runt jorden under din livstid</p>
   </section>


   <section id="blinka" class="col-start-1 col-end-4 row-start-12 row-end-12">
       <p>Du har blinkat {blinka} gånger</p>
   </section>


   <section id="sova" class="col-start-1 col-end-4 row-start-13 row-end-13">
       <p>Du har sovit i {sova} dagar.</p>
   </section>


   <section id="sova2" class="col-start-1 col-end-4 row-start-13 row-end-13">
       <p>Det är en tredjedel av ditt liv!</p>
   </section>


   <section id="footer" class="col-start-1 col-end-4 row-start-14 row-end-14">
       <p>Är det någonting du saknar?</p>
   </section>


   <section id="footer2" class="col-start-1 col-end-4 row-start-15 row-end-15">
       <p>Kontakta xxxxxxxxxxx@gmail.com</p>
   </section>


  




   <!-- <section id="text" class="rubrik col-start-2 row-start-2 justify-self-center">
       <img src="/Life stats text.png" alt="text">
   </section> -->
</main>




<style>
   main {
       /* background-color: rgb(121, 136, 164); */
       background-color: rgb(51, 89, 124);
       height: 100vh;
   }


   #dagarlevt {
       /* background-color: #ffffff; */
       color:#000000;
       border: none;
       display: flex;
       justify-content: center;
       padding-left: 620px;
       padding-top: 250px;
       font-size:xxx-large;
       /* background-color:rgb(18, 28, 45); */
   }


   #veckorlevt {
       /* background-color:rgb(11, 46, 106); */
       color:#000000;
       border: none;
       display: flex;
       justify-content: center;
       align-items: center;
       padding-left: 620px;
       font-size:xxx-large;
   }


   #årlevt {
       color:#000000;
       display: flex;
       justify-content: center;
       /* background-color: rgb(18, 28, 45); */
       padding-top: 525px;
       padding-left: 620px;
       font-size:xxx-large;
   }


   #andas {
       color:#000000;
       display: flex;
       justify-content: center;
       align-items: center;
       /* background-color: rgb(9, 58, 142); */
       padding-top: 300px;
       padding-left: 400px;
       font-size:xxx-large;
   }


   #hjärta {
       color:#000000;
       display: flex;
       justify-content: center;
       align-items: center;
       /* background-color: rgb(18, 28, 45); */
       padding-top: 300px;
       padding-left: 500px;
       font-size:xxx-large;
   }


   #jorden {
       color:#ffffff;
       display: flex;
       justify-content: center;
       /* background-color: rgb(10, 57, 137); */
       font-size:xxx-large;
       padding-top: 300px;
       padding-left: 600px;
   }


   #jorden2 {
       color:#ffffff;
       display: flex;
       justify-content: center;
       align-items: center;
       /* background-color: rgb(10, 57, 137); */
       font-size:xxx-large;
       padding-left: 600px;
   }


   #jorden3 {
       color:#ffffff;
       display: flex;
       justify-content: center;
       align-items: center;
       /* background-color: rgb(10, 57, 137); */
       padding-top: 200px;
       padding-left: 600px;
       font-size:xxx-large;
   }


   #blinka {
       color:#000000;
       display: flex;
       justify-content: center;
       align-items: center;
       /* background-color: rgb(18, 28, 45); */
       padding-top: 200px;
       padding-left: 150px;
       font-size:xxx-large;
   }
  
   #sova {
       color:#000000;
       display: flex;
       align-items: center;
       /* background-color: rgb(7, 48, 119); */
       font-size:xxx-large;
       padding-left: 50px;
   }


   #sova2 {
       color:#000000;
       display: flex;
       align-items: center;
       /* background-color: rgb(7, 48, 119); */
       padding-top: 150px;
       font-size:xxx-large;
       padding-left: 50px;
   }


   #skriv {
       border: none;
       border: none;
       border: solid 1px rgb(18, 28, 45);
   }


   #footer {
       /* background-color: rgb(18, 28, 45); */
       display: flex;
       justify-content: center;
       align-items: end;
       color: rgb(255, 255, 255);
       font-size: larger;
   }


   #footer2 {
       /* background-color: rgb(18, 28, 45); */
       display: flex;
       justify-content: center;
       color: rgb(255, 255, 255);
       padding: 10px;
       font-size: larger;
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
       font-size: larger;
   }


   #rubrik {
       font-family:sans-serif;
       font-weight:lighter;
       font-size: 120pt;
       color: #ffffff;
   }


   #bildbaby {
       display: flex;
       align-items: start;
       padding-left: 600px;
       padding-top: 100px;
   }


   #bildbaby img {
       width: 30%;
   }


</style>
