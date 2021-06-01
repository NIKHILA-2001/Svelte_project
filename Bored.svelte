<script>
  let b = {};
  let count = 0;
  async function getData() {
    const info = await fetch("https://www.boredapi.com/api/activity");
    const d = await info.json();
    b = d;
    count = 1;
  }
</script>

<div>
<h1>Bored!! Click here To get awesome Ideas..</h1>
<button class='btn' on:click={getData}>Get Idea</button><br>
{#if count==0}
  <div class="val">
  <h2> </h2>
  <img class="image1" src='https://c.tenor.com/QlFNdJkMUN4AAAAj/unwilling-yawning.gif' alt="">
  </div>
{/if}
{#if count==1}
<h2>{b.activity}</h2>
<img class="image" src='https://media4.giphy.com/media/oF5oUYTOhvFnO/giphy.webp?cid=ecf05e47zpu6gy2d6htxwoc4oy17t8kie3utyb4pur3q2d48&rid=giphy.webp&ct=g' alt="">
{/if}
</div>
<img class='img1' src='https://tse2.mm.bing.net/th?id=OIP.TLe5DpfDpMSkw0SDvvrA4gHaHa&pid=Api&P=0&w=300&h=300' alt="">
<img class='img2' src='https://tse2.mm.bing.net/th?id=OIP.TLe5DpfDpMSkw0SDvvrA4gHaHa&pid=Api&P=0&w=300&h=300' alt="">
<style>
  div {
    text-align: center;
  }
  .btn {
    margin: 10px;
    font-size: 31px;
    padding: 4px;
    background-color: rgb(158, 80, 173);
    color: white;
    border: none;
    border-radius: 7px;
    box-shadow: 0px 6px gray;
  }
  .btn:active {
    box-shadow: 0px 4px rgb(92, 91, 91);
    transform: translateY(4px);
  }
  .img1 {
    position: absolute;
    width: 28%;
    bottom: 0px;
    right: 0px;
    height: 51%;
    opacity: 0.7;
  }
  h2 {
    font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
    font-size: 40px;
  }
  h1 {
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    color: rgb(43, 10, 51);
    font-size: 53px;
  }
  .img2 {
    position: absolute;
    width: 20%;
    bottom: 0px;
    left: 0px;
    height: 44%;
    opacity: 0.7;
  }
  .image {
    width: 28%;
    height: 24%;
  }
  .image1 {
    width: 34%;
    height: 50%;
  }
</style>