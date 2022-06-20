<script>
  import MyButton from "../components/button.svelte";
  import Infomodecard from "../components/tilmeld_infomode_card.svelte";
  import Accordion from "../components/tilmeld_accrodian.svelte";
</script>

<header class="h-full w-full relative overflow-hidden" id="video">
  <img class="hero-image" src="infomode.webp" alt="" />
  <div class="hero-text m-auto">
    <p class="text-white">FÅ SVAR PÅ ALLE DINE SPØRGSMÅL OG</p>
    <h1 class="">VÆR MED TIL VORES INFOAFTEN</h1>
  </div>

  <div class="absolute z-50 bottom-14 left-[calc(50%-25px)] h-12 w-auto">
    <img class="h-auto w-12" src="scroll_down.png" alt="scroll down icon" />
  </div>
</header>

<div class="m-9 broedkrummer">
  <a href="index">Forside /</a>
  <a href="alleophold" class="underline broedkrummer">Infoaften </a>
</div>

<main>
  <section class="maxwidthwrapper">
    <p class="preh2 text-center m-auto">GRATIS & UFORPLIGTENDE</p>
    <h2 class="text-center m-auto">INFOAFTEN & REJSEFEBER CAFÉ</h2>
    <p class="text-center m-auto">
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
      src="solnedgang-2.webp"
      alt="instagram - Hygge i golden hour"
    />
    <div class="col-start-1 row-start-1 mt-10">
      <p class="preh2">GRATIS & UFORPLIGTENDE</p>
      <h2>MØD OS OG BLIV INSPIRERET</h2>
      <p>
        Hvis du drømmer om et fantastisk rejseeventyr med masser af adventure,
        vilde naturoplevelser, spændende kulturmøder og et stærkt
        højskole-fællesskab, så hop med på et af vores hyggelige infoaften. Du
        møder Thomas, Amadeus eller Emil (ejerne af HÖJSKOLENDK) og nogle af
        vores skønne elever.
      </p>
      <div class="mt-5">
        <MyButton type="primary">JOIN OS TIL INFOAFTEN</MyButton>
      </div>
    </div>
  </section>

  <section class="section_2 text-center md:mt-10 md:mb-10">
    <div class="text-center ">
      <p class="preh2 ml-auto mr-auto">BÅDE ONLINE OG FYSISK</p>
      <h2 class="ml-auto mr-auto">Det får du ud af infoaftenen</h2>
    </div>
    <div class="bgfooter overflow-hidden">
      <div class="maxwidthwrapper">
        <div class="footer_kontakt flex gap-10 justify-center m-auto pt-8">
          <div>
            <!-- hvid cirkel -->
            <div class="cirkel m-auto grid justify-center">
              <img
                id="special_icon"
                class=" m-auto"
                src="icon_qmark.png"
                alt="blog ikon"
              />
            </div>
            <p class="tabeltxt">Få svar på dine spørgsmål</p>
          </div>
          <div>
            <!-- hvid cirkel -->
            <div>
              <div class="cirkel m-auto grid justify-center">
                <img class="m-auto" src="swag.png" alt="brev ikon" />
              </div>
              <p class="tabeltxt">Få sat ansigt på HÖJSKOLENDK</p>
            </div>
          </div>
          <div>
            <!-- hvid cirkel -->
            <div>
              <div class="cirkel m-auto grid justify-center">
                <img class="m-auto" src="icon_ophold.png" alt="chat ikon" />
              </div>
              <p class="tabeltxt">Lær mere vores enventyrlige ophold</p>
            </div>
          </div>
          <div>
            <!-- hvid cirkel -->
            <div>
              <div class="cirkel m-auto grid justify-center">
                <img class="m-auto" src="faelleskab.png" alt="brev ikon" />
              </div>
              <p class="tabeltxt">Mød vores skønne tidligere elver</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="maxwidthwrapper grid gap-10">
    <div>
      <p class="preh2">ONLINE OG FYSISKE MØDER</p>
      <h2>KOMMENDE INFOAFTENER</h2>
    </div>
    <Accordion
      dag="19"
      month="JUN"
      title="Infoaften København"
      subtitle="For dig der drømmer om dit livs eventyr"
      tid="Kl. 17:00 - 19:00"
      vej="Købmagergade 29,"
      by=" 1970 Købbenhavn K"
    />
    <Accordion
      dag="23"
      month="JUL"
      title="Infoaften Aarhus"
      subtitle="For dig der drømmer om dit livs eventyr"
      tid="Kl. 17:00 - 19:00"
      vej="Vestergade 49,"
      by="8000 Aarhus C"
    />
    <Accordion
      dag="12"
      month="AUG"
      title="Infoaften Online"
      subtitle="For dig der drømmer om dit livs eventyr"
      tid="Kl. 17:00 - 19:00"
      vej="Online,"
      by="Vi sender dig et link"
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

  .section_2 {
    background-color: var(--sandbeach);
  }

  .footer_kontakt img {
    width: 42px;
    height: 42px;
  }

  .footer_kontakt {
    display: grid;
    grid-template-columns: 1fr 1fr;
    max-width: 100px;
  }

  .cirkel {
    width: 100px;
    height: 100px;
    background-color: white;
    border-radius: 100px;
    margin: auto;
  }

  #special_icon {
    width: 30px;
    height: 42px;
  }

  @media screen and (min-width: 700px) {
    .footer_kontakt {
      grid-template-columns: 1fr 1fr 1fr 1fr;
      max-width: 600px;
    }
    .footer_kontakt img {
      margin: auto;
    }
  }
</style>
