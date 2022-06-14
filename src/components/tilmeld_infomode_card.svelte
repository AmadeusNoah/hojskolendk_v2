<script>
  export let dato;
  export let title;
  export let subtitle;
  export let tid;
  export let adresse;
</script>

<section
  class="ophold max-w-full xl:max-h-[300px] block sm:grid sm:grid-cols-2 items-center sm:pb-0 gap-6 xl:flex"
>
  <div class="h-full grids-start-1 xl:max-w-[500px] ">
    <p>{dato}</p>
  </div>

  <div class="p-4 md:grid gap-4 xl:gap-7 grids-start-2">
    <div class="">
      <h3>{title}</h3>
      <p>{subtitle}</p>
    </div>
    <div class="xl:flex xl:gap-7">
      <div class="flex mt-5 lg:mt-0 gap-4 items-center">
        <img class="w-8 h-8 " src="calender.png" alt="kalender ikon" />
        <div>
          <p class="">Tid:</p>
          <p class="tabeltxt">{tid}</p>
        </div>

        <div class="h-10 bg-slate-400 w-0.5 hidden xl:block" />
      </div>

      <div class="flex mt-5 lg:mt-0 gap-4  items-center">
        <img class="w-8 h-8" src="price.png" alt="pris ikon" />
        <div class="w-22">
          <p class="">Adresse:</p>
          <p class="tabeltxt ">{adresse}</p>
        </div>
      </div>
      <div class="h-10 bg-black w-0.5 hidden" />
    </div>
    <div class="flex sm:justify-start pt-4" />
  </div>
</section>

<style>
  .ophold {
    margin: 5px;
    background-color: var(--sandstone);
    margin-bottom: 2rem;
  }

  /* Show the dropdown menu */
  .show {
    display: block;
  }
  /* 
  .right svg {
    height: 25px;
    width: 25px;
  } */

  /* .right {
    background-color: white;
    border-radius: 50px;
    height: 60px;
    width: 60px;
    z-index: 10;
  } */

  @media screen and (max-width: 400px) {
    section {
      max-width: 100px;
    }
  }
</style>
