<script>
  let name;
  let info = {};
  let count = 0;
  async function data() {
    count = 1;
    const fetch_data = await fetch("https://api.genderize.io/?name=" + name);
    const d = await fetch_data.json();
    info = d;
    document.querySelector(".inp").value = "";
  }
</script>

<div class="container">
   <h1>Give name and predict Gender </h1>
   <input bind:value={name} class="inp" type="text" placeholder="enter a name">
   <button on:click={data} class='btn' >
    Predict Gender
   </button>
    <div>
    {#if count==1}
      <p><strong>Given Name :</strong> {info.name}</p>
      <p><strong>Gender : </strong>{info.gender}</p>
      <p><strong>Probability Chance : </strong>{info.probability}</p>
    {:else}
       <h2>🤗Hii !!</h2>
    {/if}
    <img class='img' src='https://previews.123rf.com/images/blueringmedia/blueringmedia1706/blueringmedia170600994/80862554-opposite-wordcard-for-male-and-female-illustration.jpg' alt=" ">
    <img class='img2' src='https://image.freepik.com/free-vector/set-cute-boy-girl_1308-28938.jpg' alt=" ">
    </div>
</div>

<style>
  div {
    font-family: cursive;
    text-align: center;
  }
  .btn {
    display: inline-block;
    margin-top: 5px;
    border-radius: 7px;
    padding: 5px;
    color: white;
    font-weight: 400;
    background-color: rgb(45, 218, 160);
    box-shadow: 0px 6px rgb(158, 157, 157);
    font-size: 25px;
    border: none;
  }
  .inp {
    outline-style: Chance;
    outline: none;
    border: none;
    font-size: 2em;
    margin: 15px;
    text-align: center;
    box-shadow: 3px 3px 5px #ccc;
  }
  p {
    font-family: monospace;
    font-size: 3em;
  }
  h1 {
    font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
    font-size: 60px;
    color: purple;
    text-shadow: 2px 2px 2px #ccc;
    padding: 7px;
  }
  h2 {
    font-size: 3em;
    padding: 10px;
  }
  .btn:active {
    box-shadow: 0px 4px rgb(92, 91, 91);
    transform: translateY(4px);
  }
  .img {
    position: absolute;
    width: 28%;
    bottom: 8px;
    right: 2px;
    height: 55%;
    opacity: 0.8;
  }
  .img2 {
    position: absolute;
    width: 23%;
    bottom: 8px;
    left: 2px;
    height: 43%;
    opacity: 0.8;
  }
</style>