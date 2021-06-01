<script>
  let joke = {};
  async function getData() {
    const info = await fetch("https://official-joke-api.appspot.com/random_joke");
    const d = await info.json();
    joke = d;
    console.log(joke);
  }
</script>

<div>
<h1>Laugh along with us with Sarcastic Jokes 😛</h1>
<button class='btn' on:click={getData}>NEW JOKE</button><br>
{#if joke.setup!=undefined}
<h2>{joke.setup}</h2>
<h2>{joke.punchline}</h2>
{/if}
<img src='https://i.giphy.com/media/Fn7q3cMgPZmqk/giphy.webp' alt='Saradaga Kasepu Navvukondi Prends'>
</div>

<style>
  div {
    background: url("https://media.istockphoto.com/photos/blank-abstract-light-blue-watercolor-background-isolated-on-white-picture-id515009713?k=6&m=515009713&s=170667a&w=0&h=KnIReXHdzJs7zjKq4MEvFVtU1AiEQNAowBfSlmF6-p4=");
    background-size: cover;
    text-align: center;
    margin: 10px;
  }
  .btn {
    margin: 25px;
    font-size: 31px;
    padding: 4px;
    background-color: rgb(177, 206, 47);
    color: white;
    border: none;
    border-radius: 7px;
    box-shadow: 0px 6px rgb(150, 149, 149);
  }
  .btn:active {
    box-shadow: 0px 4px rgb(107, 107, 107);
    transform: translateY(4px);
  }
  h1 {
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    color: rgb(4, 43, 23);
    font-size: 53px;
  }
  h2 {
    font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
    font-size: 40px;
  }
</style>
