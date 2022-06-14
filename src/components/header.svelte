<script>
  export let imgtitle;
</script>

<div>
  <img src={imgtitle} alt="herobillede" class="hero-image" />
  <div class="hero-text">
    <p>Rejs med HÖJSKOLENDK til</p>
    <h1>SRI LANKA, MALDIVERNE <br /> & THAILAND</h1>
  </div>

  <div class="absolute z-50 bottom-24 left-[calc(50%-25px)] h-12 w-auto">
    <img class="h-auto w-12" src="scroll_down.png" alt="scroll down icon">
  </div>
</div>

<style>
  .hero-text h1,
  p {
    color: var(--hvid);
  }
</style>
