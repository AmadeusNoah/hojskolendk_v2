<script>
  import Header from "../components/header.svelte";
  import Infomodecard from "../components/infomode_card.svelte";
</script>

<header class="h-full w-full relative overflow-hidden" id="video">
  <img src="" alt="" />
  <div class="hero-text m-auto">
    <p class="text-white">FÅ SVAR PÅ ALLE DINE SPØRGSMÅL OG</p>
    <h1 class="">VÆR MED TIL VORES INFOMØDER</h1>
  </div>

  <div class="absolute z-50 bottom-14 left-[calc(50%-25px)] h-12 w-auto">
    <img class="h-auto w-12" src="scroll_down.png" alt="scroll down icon" />
  </div>
  <div class="wave absolute bottom-[6px]">
    <svg
      width="3311"
      height="69"
      viewBox="0 0 3311 69"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M1117.7 32.6112C407.753 27.7762 99.6691 49.7522 0 66.7752V69L170.798 67.9949H640.254H3311V32.6112V0C3214.82 13.0946 2921.85 49.8962 2519.46 56.1817C2016.46 64.0384 2005.13 38.6548 1117.7 32.6112Z"
        fill="white"
      />
    </svg>
  </div>
</header>

<div class="m-9 broedkrummer">
  <a href="index">Forside /</a>
  <a href="alleophold" class="underline broedkrummer"
    >Infomøder
  </a> 
</div>


<main>
  <section class="maxwidthwrapper">
    <p class="preh2">GRATIS & UFORPLIGTENDE</p>
    <h2>INFOMØDER & REJSEFEBER CAFÉ</h2>
    <p>
      Hør meget mere om vores højskoleophold i udlandet og møde nogle af vores
      skønne tidligere elever til en aften med billeder, historier og gode
      vibes. Vi fortæller meget mere om de rejseeventyr som venter!
    </p>
    <br />
    <hr />
  </section>

  <section class="maxwidthwrapper">
    <div>
      <p class="preh2">GRATIS & UFORPLIGTENDE</p>
      <h2>MØD OS OG BLIV KLOGERE</h2>
      <p>
        Hvis du drømmer om et fantastisk rejseeventyr med masser af adventure,
        vilde naturoplevelser, spændende kulturmøder og et stærkt
        højskole-fællesskab, så hop med på et af vores hyggelige infomøder. Du
        møder Thomas, Amadeus eller Emil (ejerne af HÖJSKOLENDK), nogle af vores
        skønne tidligere elever.
      </p>
      <button>TILMELD DIG INFOMØDE</button>
    </div>
    <img src="" alt="" />
  </section>

  <section class="maxwidthwrapper grid gap-10">
    <h3>Maj 2022</h3>
    <Infomodecard
      image="stud_kbh.webp"
      title="Infomøde København"
      subtitle="For dig der drømmer om dit livs eventyr"
      dato="06 Maj 22"
      tid="Kl. 17:00 - 19:00"
      adresse="Studenterhuset København Købmagergade 29, 1970 Købbenhavn K"
    />
    <Infomodecard
      image="stud_odense.webp"
      title="Infomøde Odense"
      subtitle="For dig der drømmer om dit livs eventyr"
      dato="10 Maj 22"
      tid="Kl. 17:00 - 19:00"
      adresse="Studenterhuset Aarhus
Købmagergade 29,
1970 Aarhus"
    />
    <Infomodecard
      image="zoom.webp"
      title="Online Infomøde"
      subtitle="For dig der drømmer om dit livs eventyr"
      dato="12 Maj 22"
      tid="Kl. 17:00 - 19:00"
      adresse="Zoom.com"
    />
  </section>

  <section class="maxwidthwrapper grid">
    <h3>Juni 2022</h3>
    <Infomodecard
      image="stud_kbh.webp"
      title="Infomøde København"
      subtitle="For dig der drømmer om dit livs eventyr"
      dato="06 Juni 22"
      tid="Kl. 17:00 - 19:00"
      adresse="Studenterhuset København Købmagergade 29, 1970 Købbenhavn K"
    />
  </section>
</main>

<style>
  main {
    background-image: url(src/_icons/gurfers.png);
    background-position: cover;
    background-size: 200%;
    background-repeat: repeat-y;
    background-position-x: 10%;
  }

  section {
    padding-top: var(--padding-sections);
    padding-bottom: var(--padding-sections);
  }
</style>
