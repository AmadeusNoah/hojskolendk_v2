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

<div
  class="maxwidthwrapper max-w-fit  accordion custom_grid w-full block items-center mb-4"
>
  <div class=" md:grid-rows-1 xl:max-w-[500px]">
    <div class="custom-border justify-center items-center ">
      <h2 class="special text-center -mb-2 p-0">{dag}</h2>
      <h3 class="text-center mb-2 p-0">{month}</h3>
      <div class="streg h-0.5 w-full md:hidden" />
    </div>
  </div>

  <div class="p-4 gap-4 xl:gap-7">
    <div class="">
      <h4>{title}</h4>
      <p>{tid}</p>
    </div>

    <!-- <div class="md:flex md:gap-10 mt-4">
      <div class="flex mt-5 lg:mt-0 gap-4  items-center">
        <img class="w-6 h-8" src="destination.png" alt="pris ikon" />
        <div class="w-22">
          <p class="font-bold">Adresse:</p>
          <p class="tabeltxt ">{vej}</p>
          <p class="tabeltxt ">{by}</p>
        </div>
        <div class="hidden md:block streg h-10 w-0.5 ml-3" />
      </div>
      <div class="flex mt-5 lg:mt-0 gap-4">
        <img class="w-8 h-8 self-center" src="clock.png" alt="kalender ikon" />
        <div>
          <p class="font-bold">Tid:</p>
          <p class="tabeltxt">{tid}</p>
        </div>
      </div>
      <div class="h-10 bg-black w-0.5 hidden" />
    </div> -->
    <div class="flex sm:justify-start pt-4" />
  </div>
  <button class="ml-4" on:click={handleClick}
    >{!open ? "TILMELD DIG INFOMØDE" : "LUK"}</button
  >

  {#if open}
    <div class="details custom_column" transition:slide>
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
    font-size: 0.75rem;
    font-weight: bold;
    font-family: "Lato", sans-serif;
    background-color: var(--primary-button-cta-background-color);
    border: 1px solid var(--secondary-button-cta-border-color);
    color: var(--hvid);
    padding: 0.5rem 15px;
    display: inline-block;
    box-shadow: inset 0 0 0 0 var(--orange-800);
    -webkit-transition: ease-out 0.4s;
    -moz-transition: ease-out 0.4s;
    transition: ease-out 0.4s;
    white-space: nowrap;
    width: 11.5rem;
    height: 3rem;
    margin: 2rem;
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

  h2 {
    font-family: var(--h4_text);
  }
  h3 {
    font-size: var(--h4_text);
  }

  h4 {
    font-family: var(--h2_text);
    color: var(--textcolor-700);
  }

  p {
    font-size: var(--font_p_tabel);
  }

  @media screen and (min-width: 800px) {
    .custom_grid {
      display: grid;
      grid-template-columns: 0.75fr 2fr 1fr;
    }

    .custom_column {
      grid-column: 1 / 4;
    }

    .custom-border {
      border-width: 0 3px 0 0;
      border-style: solid;
      border-color: var(--txtcolor);
      margin-right: 2rem;
    }
  }
</style>
