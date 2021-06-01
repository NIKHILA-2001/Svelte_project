<script>
  let facts = [];
  async function getData() {
    const data = await fetch("https://cat-fact.herokuapp.com/facts");
    const d = await data.json();
    facts = d;
    console.log(facts);
  }
</script>
<main>
  <button on:click={getData}>GET FACT</button>
  {#each facts as fact}
    <div style="
    border-radius:4px;box-shadow:1px 2px 4px black;margin: 20px;padding:10px">
    <h2>{fact.type} fact</h2>
    <h2>{fact.text}</h2>
    </div>
  {/each}
</main>
<style>
  main {
    background: url("https://wallpapercave.com/wp/FfMvGj9.jpg");
    font-family: sans-serif;
    text-align: center;
    flex-direction: column;
    opacity: 0.7;
  }
  button {
    padding: 10px;
    font-size: 20px;
    font-weight: 600;
    background-color: rgb(21, 42, 58);
    color: white;
    border: none;
    border-radius: 4px;
    margin: 7px;
  }
  h2 {
    background-color: rcb(255, 255, 255, 0.7);
    font-size: 30px;
    font-weight: bold;
  }
</style>