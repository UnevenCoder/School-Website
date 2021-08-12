<script>
  let width = screen.width;
  let display = 0; // checkin which nav is clicked
  // Getting components
  import Home from "./Home.svelte";
</script>

<!--Desktop-->
{#if width > 800}
  <main class="main">
    <section id="content">
      <!-- {#if display == 0}
        <Home />
      {:else if display == 1}
        <Aboutus />
      {:else if display == 2}
        <Admissions />
      {:else if display == 3}
        <Curriculum />
      {:else if display == 4}
        <Noticeboard />
      {:else if display == 5}
        <Activities />
      {:else}
        <Gallery />
      {/if}-->
      <Home />
    </section>
  </main>
{/if}

<style>
  @import url("https://fonts.googleapis.com/css2?family=Poppins");
  .main {
    font-family: "Poppins", Arial, sans-serif;
    width: 100vw;
    max-width: 100vw;
    min-height: 100vh;
    max-height: 105vh;
    display: flex;
  }
  /* Side bar Stuff */

  /* Content Side */

  #content {
    min-width: 100vw;
    width: 100%;
    background-color: whitesmoke;
    color: white;
    display: flex;
  }
</style>
