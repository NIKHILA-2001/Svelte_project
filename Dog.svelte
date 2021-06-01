<script>
  let dog = {};
  let url;
  async function getData() {
    const info = await fetch("https://dog.ceo/api/breeds/image/random");
    const d = await info.json();
    dog = d;
    url = dog.message;
  }
</script>

<div>
<h1>See Cute Doggie Images..😁😍</h1>
<button class='btn' on:click={getData}>Get Image</button><br>
<img class='image' src='{url}' alt="Dogie Image">
</div>
<img class='img1' src='https://tse1.mm.bing.net/th?id=OIP.aD7QMGLoQSyPlxpXxI68gQHaHa&pid=Api&P=0&w=300&h=300' alt="">
<img class='img2' src='https://tse1.mm.bing.net/th?id=OIP.aD7QMGLoQSyPlxpXxI68gQHaHa&pid=Api&P=0&w=300&h=300' alt="">
<style>
  div {
    text-align: center;
  }
  .btn {
    margin: 10px;
    font-size: 31px;
    padding: 4px;
    background-color: rgb(107, 168, 168);
    color: white;
    border: none;
    border-radius: 7px;
    box-shadow: 0px 6px gray;
  }
  .image {
    width: 50%;
    height: 500px;
    box-shadow: 2px 3px 5px #ccc;
  }
  h1 {
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    color: rgb(10, 28, 51);
    font-size: 53px;
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
