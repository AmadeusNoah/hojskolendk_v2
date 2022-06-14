<script>
  import MyButton from "../components/button.svelte";
  import Infomodecard from "../components/tilmeld_infomode_card.svelte";
  import Accordion from "../components/tilmeld_accrodian.svelte";
</script>

<header class="h-full w-full relative overflow-hidden" id="video">
  <img class="hero-image" src="infomode.webp" alt="" />
  <div class="hero-text m-auto">
    <p class="text-white">FÅ SVAR PÅ ALLE DINE SPØRGSMÅL OG</p>
    <h1 class="">VÆR MED TIL VORES INFOMØDER</h1>
  </div>

  <div class="absolute z-50 bottom-14 left-[calc(50%-25px)] h-12 w-auto">
    <img class="h-auto w-12" src="scroll_down.png" alt="scroll down icon" />
  </div>
</header>

<div class="m-9 broedkrummer">
  <a href="index">Forside /</a>
  <a href="alleophold" class="underline broedkrummer">Infomøder </a>
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

  <section class="maxwidthwrapper md:grid grid-cols-2 md:gap-10 lg:gap-20">
    <img
      class="col-start-2 row-start-1"
      src="solnedgang.webp"
      alt="instagram - Hygge i golden hour"
    />
    <div class="col-start-1 row-start-1 mt-10">
      <p class="preh2">GRATIS & UFORPLIGTENDE</p>
      <h2>MØD OS OG BLIV KLOGERE</h2>
      <p>
        Hvis du drømmer om et fantastisk rejseeventyr med masser af adventure,
        vilde naturoplevelser, spændende kulturmøder og et stærkt
        højskole-fællesskab, så hop med på et af vores hyggelige infomøder. Du
        møder Thomas, Amadeus eller Emil (ejerne af HÖJSKOLENDK), nogle af vores
        skønne tidligere elever.
      </p>
      <div class="mt-5">
        <MyButton type="primary">JOIN OS TIL INFOMØDE</MyButton>
      </div>
    </div>
  </section>

  <section>
    <div class="text-center content-center justify-center">
      <p class="preh2">ONLINE OG FYSISKE MØDER</p>
      <h2>Det får du ud af opholdet</h2>
    </div>
  </section>

  <Accordion
    dag="19"
    month="JUN"
    title="Infomøde København"
    subtitle="For dig der drømmer om dit livs eventyr"
    tid="Kl. 17:00 - 19:00"
    vej="Købmagergade 29,"
    by=" 1970 Købbenhavn K"
  />

  <!-- <section class="maxwidthwrapper grid gap-10">
    <div>
      <p class="preh2">ONLINE OG FYSISKE MØDER</p>
      <h2>KOMMENDE INFOMØDER</h2>
    </div>
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
  </section> -->
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
