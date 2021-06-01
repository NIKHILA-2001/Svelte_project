<script>
  let fox = {};
  let url;
  async function getData() {
    const info = await fetch("https://randomfox.ca/floof/?ref=apilist.fun");
    const d = await info.json();
    fox = d;
    url = fox.image;
  }
</script>

<div>
<button class='btn' on:click={getData}>Get Image</button><br>
{#if {fox}!=undefined}
<img class='image' src='{url}' alt="Fox Image">
{/if}
</div>
<img class='img2' src='https://tse2.mm.bing.net/th?id=OIP.I4ppkoCj4rkFrlAMzqyH6AHaE3&pid=Api&P=0&w=264&h=174' alt="">
<img class='img1' src='https://tse2.mm.bing.net/th?id=OIP.I4ppkoCj4rkFrlAMzqyH6AHaE3&pid=Api&P=0&w=264&h=174' alt="">

<style>
  div {
    text-align: center;
  }
  .btn {
    margin: 10px;
    font-size: 31px;
    background-color: palevioletred;
    color: white;
    border: none;
    border-radius: 7px;
    box-shadow: 0px 6px rgb(141, 139, 139);
  }
  .image {
    width: 50%;
    height: 500px;
    box-shadow: 0px 4px #ccc;
  }
  .btn:active {
    box-shadow: 0px 4px rgb(92, 91, 91);
    transform: translateY(4px);
  }
  .img1 {
    position: absolute;
    width: 24%;
    bottom: 8px;
    right: 2px;
    height: 50%;
    opacity: 0.8;
  }
  .img2 {
    position: absolute;
    width: 20%;
    bottom: 8px;
    left: 2px;
    height: 40%;
    opacity: 0.8;
  }
</style>
