<script>
  let option = 0;
  import Dog from "./Dog.svelte";
  import Bore from "./Bored.svelte";
  import Fox from "./Fox.svelte";
  import Gender from "./Gender.svelte";
  import Joke from "./Jokes.svelte";
  import Start from "./Start.svelte";
  function fun1() {
    if (option == 1) {
      option = 0;
    } else {
      option = 1;
    }
  }
  function fun2() {
    option = 2;
  }
  function fun3() {
    option = 3;
  }
  function fun4() {
    option = 4;
  }
  function fun5() {
    option = 5;
  }
</script>
{#if option==0}
 <div>
  <Start/>
	<button on:click={fun1} class='btn_s'>Click here to see
  <br> projects Using API</button>
</div>
{/if}
<div class="main_b">
  {#if option>=1}
   <button class='ar_btn' 
   on:click={fun1}>◀</button>
  {/if}

  {#if option==1}
  <main >
  <h1>Choose Your Option</h1>
	<button on:click={fun2} class='btn'>Gender Prediction</button>
  <button on:click={fun3} class='btn'>Bored! click here.</button>
	<button on:click={fun4} class='btn'>Dog images</button>
	<button on:click={fun5} class='btn'>Jokes</button>
  </main>
  {/if}
  {#if option==2}
   <Gender/>
  {/if}
  {#if option==3}
  <Bore/>
  {/if}
  {#if option==4}
  <Dog/>
  {/if}
  {#if option==5}
  <Joke/>
  {/if}
</div>
<style>
  .main_b {
    align-items: center;
  }
  .ar_btn {
    font-size: 20px;
    display: inline-block;
    background-color: orangered;
    color: white;
    border: none;
    box-shadow: 0 4px #999;
    font-weight: 900;
    border-radius: 16px;
    padding-left: 8px;
    padding-right: 10px;
  }
  main {
    background: url("https://static4.arrow.com/-/media/arrow/images/research-and-events/videos/0520/api-video-page/approved/revised/api_background.jpg");
    background-size: cover;
    text-align: center;
    display: flex;
    flex-direction: column;
    padding: 20px;
    margin: 20px;
  }
  .btn {
    padding: 16px;
    margin-left: 30%;
    margin-top: 25px;
    margin-bottom: 3.5%;
    font-size: 2em;
    font-weight: bold;
    border-radius: 40px;
    border: none;
    width: 550px;
    background-color: rgb(255, 255, 255, 0.3);
    box-shadow: 3px 3px 6px;
  }
  h1 {
    font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
    font-family: monospace;
    font-size: 50px;
    font-weight: bold;
    color: whitesmoke;
    text-shadow: 1px 1px 3px white;
    margin: 15px;
    margin-bottom: 25px;
  }
  .btn_s {
    margin: 5px;
    padding: 6px;
    border-radius: 4px;
    position: absolute;
    top: 20%;
    font-size: 20px;
    color: white;
    font-weight: bold;
    background-color: yellowgreen;
    right: 20px;
    box-shadow: 2px 2px 4px black;
    position: fixed;
  }
  .btn_s:hover {
    margin: 8px;
    font-size: 22px;
    background-color: rgb(144, 136, 36);
    transition: 0.3s;
  }
  .btn:hover {
    padding: 17px;
    font-size: 2.1em;
    transition: 0.3s;
  }
  .ar_btn:hover {
    background-color: rgb(218, 76, 11);
  }
  .ar_btn:active {
    box-shadow: 0 3px #666;
    transform: translateY(4px);
  }
  @media screen and (max-width: 800px) {
    .btn {
      margin: 20px;
    }
  }
</style>