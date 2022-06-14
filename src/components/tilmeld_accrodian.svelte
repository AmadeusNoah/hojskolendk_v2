<script>
  import { slide } from "svelte/transition";
  const handleClick = () => (open = !open);
  import InfomodeCard from "../components/tilmeld_infomode_card.svelte";

  export let dag;
  export let month;
  export let title;
  export let subtitle;
  export let tid;
  export let vej;
  export let by;

  let open = false;
  let inputValue = "";
  $: console.log(inputValue);
</script>

<div class="accordion w-full md:grid">
  <div
    class="h-full grids-start-1 md:col-start-1 md:grid-rows-1 xl:max-w-[500px] "
  >
    <h2 class=" text-center">{dag}</h2>
    <h2 class="text-center">{month}</h2>
    <div class="streg h-0.5 w-full md:hidden" />
  </div>

  <div
    class="p-4 md:grid gap-4 xl:gap-7 grids-start-2  md:col-start-2 md:grid-rows-1"
  >
    <div class="">
      <h3>{title}</h3>
      <p>{subtitle}</p>
    </div>
    <div class="xl:flex xl:gap-7">
      <div class="flex mt-5 lg:mt-0 gap-4  items-center">
        <img class="w-8 h-8" src="destination.png" alt="pris ikon" />
        <div class="w-22">
          <p class="">Adresse:</p>
          <p class="tabeltxt ">{vej}</p>
          <p class="tabeltxt ">{by}</p>
        </div>
      </div>
      <div class="flex mt-5 lg:mt-0 gap-4 items-center">
        <img class="w-8 h-8 " src="clock.png" alt="kalender ikon" />
        <div>
          <p class="">Tid:</p>
          <p class="tabeltxt">{tid}</p>
        </div>

        <div class="h-10 bg-slate-400 w-0.5 hidden xl:block" />
      </div>
      <div class="h-10 bg-black w-0.5 hidden" />
    </div>
    <div class="flex sm:justify-start pt-4" />
  </div>
  <button class=" md:col-start-3 md:grid-rows-1" on:click={handleClick}
    >{!open ? "TILMELD DIG INFOMØDE" : "PIK"}</button
  >

  {#if open}
    <div class="details md:col-start-1 md:grid-rows-2" transition:slide>
      <InfomodeCard
        image="stud_kbh.webp"
        title="Infomøde København"
        subtitle="For dig der drømmer om dit livs eventyr"
        dato="06 Maj 22"
        tid="Kl. 17:00 - 19:00"
        adresse="Studenterhuset København Købmagergade 29, 1970 Købbenhavn K"
      />
    </div>
  {/if}
</div>

<style>
  button {
    font-size: var(--knapsize);
    font-weight: bold;
    font-family: "Lato", sans-serif;
    background-color: var(--primary-button-cta-background-color);
    border: 1px solid var(--secondary-button-cta-border-color);
    color: var(--hvid);
    padding: 0.5rem 30px;
    display: inline-block;
    box-shadow: inset 0 0 0 0 var(--orange-800);
    -webkit-transition: ease-out 0.4s;
    -moz-transition: ease-out 0.4s;
    transition: ease-out 0.4s;
    white-space: nowrap;
    width: 18rem;
    height: 4rem;
    justify-content: center;
  }

  button:hover {
    border: 1px solid var(--orange-light);
    box-shadow: inset 400px 0 0 0
      var(--primary-button-cta-background-color-hover);
    color: var(--hvid);
  }

  .accordion {
    background-color: var(--sandstone);
  }

  .streg {
    background-color: var(--txtcolor);
  }

  h3 {
    font-family: var(--h2_text);
    font-size: var(--font_h2);
    color: var(--textcolor-700);
  }
</style>
