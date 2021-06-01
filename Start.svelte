<script>
import Dog from "./Dog.svelte";
import Gender from "./Gender.svelte";
</script>

<main>
  <img class='h_img' src='https://www.vectorcast.com/sites/default/files/styles/large/public/api-icon.png?itok=bDuDClfU'
  alt='What is an API'>
  <img class="point"
   src='https://hotemoji.com/images/emoji/l/17zcrtb11cx2zl.png' alt="">
	<hr>
  <h2>What is an API?</h2>
  <p>APIs — that is, Application Programming Interfaces —
   play a bigger role in today’s economy than ever before.
  They allow us to share important data and expose practical
  business functionality between devices, applications, and 
  individuals. And although we may not notice them, APIs really
  are everywhere, powering our lives from behind the scenes.
  In computing, an application programming interface (API) is an 
  interface that defines interactions between multiple software applications or 
  mixed hardware-software intermediaries.<br>[1] It defines the kinds
   of calls or requests that can be made, how to make them,
    the data formats that should be used, the conventions
     to follow, etc. It can also provide extension mechanisms so 
     that users can extend existing functionality in various ways
  and to varying degrees.<br>[2] An API can be entirely custom, specific to a component,
   or designed based on an industry-standard to ensure 
   interoperability. Through information hiding, APIs enable modular 
   programming, allowing users to use the interface independently 
   of the implementation.
Reference to Web APIs is currently the most common use of the
 term.<br>[3] There are also APIs for programming languages,
  software libraries, computer operating systems, and computer
   hardware. APIs originated in the 1940s, though the term API 
   did not emerge until the 1960s and 70s.</p>
  <h2>How does an API look like?</h2>
  <details>
  <img class="ex_img" src='https://i.stack.imgur.com/95OK5.png' alt="API EXAMPLE">
  <p>API is represented in JSON format , with key:value pairs.<br>
  API's are in the form of url called as endpoint.
  &nbsp;Example: <br><br>
  Here are some endpoints:<br>
   <a 
   href="https://api.apify.com/v2/datasets/58a4VXwBBF0HtxuQa/items?format=json&clean=1" >
    &nbsp;<li>Covid APi</li> </a> 
   <a 
   href="https://jobs.github.com/positions.json?description=api" >
    &nbsp;<li>Github Jobs API</li> </a>
  <a 
   href="https://cat-fact.herokuapp.com/facts">
    &nbsp;<li>Cat-fact</li> </a> 
    <a 
   href="https://api.genderize.io?name=luc">
    &nbsp;<li>Gender</li> </a> 
   </p>
   </details>
   <summary>
   </summary>
   <h2>Usage ?</h2>
   <details>
   <img style="float:right;margin:4px;"
    src='https://19yw4b240vb03ws8qm25h366-wpengine.netdna-ssl.com/wp-content/uploads/Login-using-social-APIs-400x254.png' alt="">
    <p>In building applications, an API (application programming
     interface) simplifies programming by abstracting the
      underlying implementation and only exposing objects or 
       actions the developer needs. While a graphical interface for
    an email client might provide a user with a button that
    performs all the steps for fetching and highlighting 
    new emails, an API for file input/output might give the 
    developer a function that copies a file from one location 
    to another without requiring that the developer understand
     the file system operations occurring behind the scenes.
     <br>&nbsp;Another prominent example of API usage is the “log-in using
      Facebook/Twitter/Google/Github” functionality you see on so many websites.
       It’s incredibly convenient, but have you ever wondered how it works?<br>
Instead of actually logging-in to users’ social media accounts 
(which would pose a serious security concern), applications with this functionality
 leverage these platforms’ APIs to authenticate the user with each login. For example, 
 here’s the Facebook Login API.<br>&nbsp;&nbsp
 The way it works is pretty simple. Every time the application loads, it uses the API
  to check whether the user is already logged in by means of whatever social media platform.
   If not, when the user clicks the “Log-in Using XYZ” button, a pop-up opens
   where they are asked to confirm they actually want to log-in with that social
  media profile. When the user confirms, the API provides the application with
  identification information, so it knows who’s logging in.
   </details>
   <summary>
   </summary>
</main>


<style>
  main {
    font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
  }
  .h_img {
    width: 18%;
    margin-left: 38%;
  }
  .ex_img {
    width: 50%;
    height: 30%;
    margin: 5px;
    float: right;
  }
  p {
    margin: 30px;
    font-size: 21px;
  }
  h2 {
    margin: 30px;
  }
  details {
    margin: 30px;
  }
  summary {
    margin: 30px;
    font-size: 20px;
  }
  .point {
    border-radius: 4px;
    position: absolute;
    top: 11%;
    width: 55px;
    font-weight: bold;
    background-color: white;
    right: 70px;
    position: fixed;
    animation-name: show;
    animation-duration: 10s;
    transition-delay: 0.1s;
  }
  @keyframes show {
    0% {
      top: 8%;
    }
    10% {
      top: 11%;
    }
    20% {
      top: 8%;
    }
    30% {
      top: 11%;
    }
    40% {
      top: 8%;
    }
    50% {
      top: 8%;
    }
    60% {
      top: 11%;
    }
    70% {
      top: 8%;
    }
    80% {
      top: 11%;
    }
    90% {
      top: 8%;
    }
    100% {
      top: 11%;
    }
  }
</style>

