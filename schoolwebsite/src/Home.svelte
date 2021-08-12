<script>
  let id = 0;
  let randomnum = Math.random() * 20;
  let x = fetch(
    "https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=10&page=" +
      randomnum +
      "&sparkline=false",
    {
      accept: "application/json",
    }
  ).then((res) => res.json());
</script>

<main>
  {#await x}
    hey
  {:then data}
    {#each data as coin}
      <div class="coin">
        <img src={coin.image} alt="" width="30px" height="30px" />
        <h6>{coin.name}</h6>
        <h6>{coin.id}</h6>
        <h6>{coin.current_price}</h6>
        <h6>{coin.total_volume}</h6>
        <h6 class={coin.price_change_24h > 0 ? "green" : "red"}>
          {coin.price_change_24h > 0 ? "+" : ""}{coin.price_change_24h.toFixed(
            2
          )}
        </h6>
        <h6>{coin.market_cap.toLocaleString()}</h6>
      </div>
    {/each}
  {/await}
</main>

<style>
  main {
    max-width: 100%;
    width: 80vw;
    min-height: 100%;
    color: #232323;
    background-color: whitesmoke;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .coin {
    width: 100%;
    display: flex;
    justify-content: space-around;
    font-size: medium;
    align-items: center;
  }
  .green {
    color: greenyellow;
  }
  .red {
    color: tomato;
  }
  .coin h6 {
    width: 60px;
    text-align: left;
  }
</style>
