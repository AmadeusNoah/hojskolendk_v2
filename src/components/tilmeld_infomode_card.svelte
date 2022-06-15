<script>
  import MyButton from "../components/button.svelte";
</script>

<section class="ophold max-w-fit block  sm:pb-0 gap-6">
  <div class="streg h-0.5 w-full " />
  <h3 class="px-8 pt-6 pb-4 mb-4">Tilmeld dig infomødet</h3>
  <div class="sm:grid sm:grid-cols-2">
    <form class=" px-8 pb-8 mb-4">
      <div class="mb-4">
        <label class="block  text-sm font-bold mb-2" for="Navn"> Navn </label>
        <input
          class=" appearance-none w-full py-2 px-3  leading-tight focus:shadow-outline"
          id="name"
          type="text"
          placeholder="Navn"
        />
      </div>
      <div class="mb-4">
        <label class="block  text-sm font-bold mb-2" for="Navn">
          Efternavn
        </label>
        <input
          class=" appearance-none w-full py-2 px-3  leading-tight focus:shadow-outline"
          id="lastname"
          type="text"
          placeholder="Efternavn"
        />
      </div>
      <div class="mb-4">
        <label class="block  text-sm font-bold mb-2" for="Navn"> Mobil </label>
        <input
          class=" appearance-none w-full py-2 px-3  leading-tight focus:shadow-outline"
          id="mobil"
          type="text"
          placeholder="Mobil"
        />
      </div>
      <div class="mb-6">
        <label class="block  text-sm font-bold mb-2" for="E-mail">
          E-mail
        </label>
        <input
          class=" appearance-none w-full py-2 px-3 mb-3 leading-tight focus:shadow-outline"
          id="email"
          type="text"
          placeholder="E-mail"
        />
        <p class="pt-6 pb-2 text-xs italic">
          *Disse felter skal udfyldes / vælges
        </p>
        <div>
          <div class="form-check">
            <input
              class="form-check-input appearance-none rounded-full h-4 w-4 border border-gray-300 bg-white checked:bg-slate-600 checked:border-slate-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer"
              type="radio"
              name="flexRadioDefault"
              id="flexRadioDefault1"
            />
            <label
              class="form-check-label inline-block text-sm italic"
              for="flexRadioDefault1"
            >
              Ja, i må gerne kontakte mig med spænende nyheder.
            </label>
          </div>
          <div class="form-check flex">
            <input
              class="form-check-input appearance-none rounded-full h-4 w-4 border border-gray-300 bg-white checked:bg-slate-600 checked:border-slate-600 focus:outline-none transition duration-200 mt-1 align-top bg-no-repeat bg-center bg-contain float-left mr-2 cursor-pointer"
              type="radio"
              name="flexRadioDefault"
              id="flexRadioDefault2"
            />
            <label
              class="form-check-label inline-block text-sm italic "
              for="flexRadioDefault2"
            >
              Jeg har læst jeres privatlivspolitik og generelle bestemmelser og
              er indforstået med begge.*
            </label>
          </div>
        </div>
      </div>
      <div class="flex items-center justify-between">
        <MyButton type="smallbutton">TILMELD DIG</MyButton>
      </div>
    </form>
    <div class="px-8 pb-8 mb-4">
      <h4 class="">Informationsmøde om højskoleophold i udlandet</h4>
      <p>Vi præsenterer vores eventyrlige højskole og fortæller en masse om:</p>
      <ul class="pt-4">
        <li>Hvem er HÖJSKOLENDK</li>
        <li>Vores eventyrlige højskoleophold</li>
        <li>Adventure, aktiviteter og alle de fede oplevelser der venter</li>
        <li>En ”almindelig” dag på højskole i udlandet</li>
        <li>Den levende og aktive måde vi underviser på</li>
        <li>Økonomi, lommepenge, pakkeliste, friuger, afrejsemødet, etc.</li>
      </ul>
    </div>
  </div>
</section>

<style>
  .ophold {
    margin: 5px;
    background-color: var(--sandstone);
    margin-bottom: 2rem;
  }

  li {
    margin-bottom: 0.5rem;
    color: var(--txtcolor-600);
  }

  ul li:before {
    content: "✓";
    margin-right: 0.5rem;
  }

  .streg {
    background-color: var(--txtcolor);
  }

  @media screen and (max-width: 400px) {
    section {
      max-width: 100px;
    }
  }
</style>
