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
  <div
    class=" grids-start-1 md:grid-rows-1 xl:max-w-[500px] divide-x-8 > * + * "
  >
    <div class=" justify-center items-center ">
      <h2 class="special text-center m-0 p-0">{dag}</h2>
      <h2 class="text-center mb-2 p-0">{month}</h2>
      <div class="streg h-0.5 w-full md:hidden" />
    </div>
  </div>

  <div class="p-4 gap-4 xl:gap-7">
    <div class="">
      <h4>{title}</h4>
    </div>

    <div class="md:flex md:gap-10 mt-4">
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
    </div>
    <div class="flex sm:justify-start pt-4" />
  </div>
  <button type="smallbutton" on:click={handleClick}
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

  .special {
    font-size: var(--font_h1);
  }

  p {
    font-size: var(--font_p_tabel);
  }
  h4 {
    font-family: var(--h2_text);
    color: var(--textcolor-700);
  }

  @media screen and (min-width: 800px) {
    .custom_grid {
      display: grid;
      grid-template-columns: 1fr 2fr 1fr;
    }

    .custom_column {
      grid-column: 1 / 4;
    }
  }
</style>
