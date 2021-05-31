<script>
  let id = 0;
</script>

<main>
  <section id="header">
    <button class={id == 0 ? "clicked" : ""} on:click={() => (id = 0)}
      >Home</button
    >
    <button on:click={() => (id = 1)} class={id == 1 ? "clicked" : ""}
      >Results</button
    ><button class={id == 2 ? "clicked" : ""} on:click={() => (id = 2)}
      >Find Us</button
    >
  </section>
  <section id="body">
    <h1>Welcome to our website</h1>
    <p>
      Delhi Public Schools, with the motto "Service Before Self", have been
      serving the Society in the field of education for the last 56 years. There
      are presently as many as 130 schools under its aegis, both in and outside
      India. The growing number of schools under this organizational umbrella
      signifies how the need to provide meaningful education to a large number
      of children, desirous of growing into educated & liberated human beings,
      has been fulfilled. Founded and managed by distinguished members and
      luminaries of society, culled from the various walks of life, the
      organization has always guided its member schools on the path of progress
      with their visionary approach & lofty ideas. Consequently, Delhi Public
      Schools have become significant portals of learning and growth of young
      minds. Our credo is to provide an all round development & sound moral
      base. Fostering character building & nurturing the inquisitive spirit of
      children, encouraging scientific temperament & strengthening social bonds,
      are our constant endeavours. Surging ahead with a spirit of healthy
      competition, balancing a successful career teamed with a contented life,
      is the gift we give to all our children. Guiding us in this effort of ours
      is Mr. Ashok Chandra, Chairman DPS Society, who is our constant beacon and
      source of strength.

      <br />
      Mr. Zia Nadwi Director
    </p>
    <img src="/images/TheDirector.png" alt="" />
  </section>
</main>

<style>
  main {
    max-width: 100%;
    height: 100%;
    background-color: #fafafa;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  main p {
    width: 60%;
    display: flex;
    flex-wrap: wrap;
  }
  #header {
    width: 80%;
    height: 75px;
    margin-top: 50px;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    background-color: #f8f9fa;
    box-shadow: 3px 3px rgba(144, 153, 144, 0.5);
    border-radius: 5px;
  }

  #header button {
    border: none;
    font-weight: 100;
    font-size: 1.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
    margin: 0;
    /* color: grey; */
    background: none;
  }
  button:hover {
    color: #3e64ff;
  }
  #body {
    margin-top: 60px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .clicked {
    color: #3e64ff;
  }
</style>
