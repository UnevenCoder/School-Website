<script>
  let width = screen.width;
</script>

<!--Desktop-->
{#if width > 800}
  <main class="main">
    <section id="sidebar">
      <div id="top" class="clicked">
        <img src="images/home_white_24dp.svg" alt="" />
        <h5>Home</h5>
      </div>
      <div>
        <img src="images/info_white_24dp.svg" alt="" />
        <h5>About Us</h5>
      </div>
      <div>
        <img src="images/description_white_24dp.svg" alt="" />
        <h5>Admissions</h5>
      </div>
      <div>
        <img src="images/book_white_24dp.svg" alt="" />
        <h5>Curiculum</h5>
      </div>
      <div>
        <img src="images/assignment_white_24dp.svg" alt="" />

        <h5>Notice Board</h5>
      </div>
      <div>
        <img src="images/view_list_white_24dp.svg" alt="" />
        <h5>Activities</h5>
      </div>

      <!-- we can add in home
      <div>
        <img src="images/filter_white_24dp.svg" alt="" />
        <h5>Gallery</h5>
      </div>
      <div>
        <img src="images/sticky_note_2_white_24dp.svg" alt="" />
        <h5>Results</h5>
      </div>
  
        <div>
        <img src="images/perm_identity_white_24dp.svg" alt="" />
        <h5>Find Us</h5>
      </div>-->
    </section>
    <div id="content" />
  </main>
{/if}

<style>
  @import url("https://fonts.googleapis.com/css2?family=Poppins");
  .main {
    font-family: "Poppins", Arial, sans-serif;
    width: 100vw;
    max-width: 100vw;
    min-height: 100vh;
    display: flex;
  }
  #sidebar {
    min-height: 100vh;
    width: 50px;
    min-width: 115px;
    display: flex;
    background-color: #3e64ff;
    flex-direction: column;
  }
  #sidebar #top {
    margin-top: 20px;
  }
  img {
    transform: scale(1.75);
  }
  #sidebar div {
    width: 100%;
    height: 125px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: aliceblue;
    font-size: large;
    flex-direction: column;
    font-weight: bold;
    /*border-bottom: 0.25px solid rgba(255, 255, 255, 0.8);*/
  }
  h5 {
    padding-top: 5px;
  }
  #sidebar div:hover {
    border-left: 5px solid white;
  }
  .clicked {
    border-left: 15px solid white;
  }
</style>
