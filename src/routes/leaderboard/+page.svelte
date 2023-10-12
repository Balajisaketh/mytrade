<script>
 import { onMount, onDestroy } from 'svelte';
 

let screenWidth = 0;
let check="empty";
onMount(() => {
  screenWidth = window.innerWidth;
  window.addEventListener('resize', updateScreenSize);

  // Cleanup event listener when the component is destroyed
  return () => {
    window.removeEventListener('resize', updateScreenSize);
  };
});

function updateScreenSize() {
  screenWidth = window.innerWidth;
}
function firstclick(){
    check="firstdiv"
    console.log(check)
}
function secondclick(){
    check="seconddiv"
    console.log(check)
}
function thirdclick(){
    check="thirddiv"
    console.log(check)
}

let selectedOption = ''; // Initialize a variable to store the selected option.
  let options = ['Networth (%)', 'Acr(%)', 'Day+Swing (%)' ,'Day(%)','Swing(%)']; 

import Fa from 'svelte-fa'
  import { faFlag, faHamburger, faHome, faList, faMessage } from '@fortawesome/free-solid-svg-icons'

</script>
<style>

@import 'bootstrap/dist/css/bootstrap.min.css';
    
    @import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
    .vertical-line {
    width: 1px; /* Set the width of the line */
     /* Make it as tall as its container */
    background-color:grey; /* Set the line color */

    display: inline-block; /* Display the line as an inline-block element */
 /* Adjust the margin to control the spacing between the lines */
  }
      .backcolor{
        background-color: grey;
        width:auto;
        height: auto;



      }
      .tabbackcolor{
        background-color: grey;

      }
      .selected {
    width: 150px;
    border: none;
     /* Adjust the width to your desired value */
  }
      .bgfront{
        background-color: white;
        width: auto;


      }
      .child{
        width:33.3%;

      }
      .child1{
        width:33.3%;
        

      }
      .mobileselect{
        width:auto;
        border: none;
      }
      .child2{
        width:33.3%;

      }
      .crypto{
        width: 25%;
      }
      .forex{
        width: 25%;
      }
      .eqty{
        width: 35%;
        
      }
      .networth{
        background-color: grey;
        height: auto;
      }
      .line{
        background-color: blue;
      }
      select:focus{
        border: none;
      }
      .element-below-div {
            margin-top: 1px; /* This will create a gap of 20 pixels between the div and the element */
            width: 2px;
            width: 100%;
        }
        .tabbgfront{
          background-color: white;
        }
  
      </style>

{#if screenWidth < 768}
<!-- Mobile layout -->
<div class="column">
  <nav class="navbar navbar-expand-lg navbar-light bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand text-white" href="#">ChartGame</a>
      <button class="navbar-toggler bg-white" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Features</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Pricing</a>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              Dropdown link
            </a>
            <ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
              <li><a class="dropdown-item" href="#">Action</a></li>
              <li><a class="dropdown-item" href="#">Another action</a></li>
              <li><a class="dropdown-item" href="#">Something else here</a></li>
            </ul>
          </li>
        </ul>
      </div>
    </div>
  </nav>
  <div class="col-10 mx-auto mt-5 d-flex flex-row    border border-2 rounded">
    <div class="eqty " class:tabbackcolor={check === 'firstdiv'} class:tabbgfront={check !== 'firstdiv'}  on:click={firstclick}>
   <p class="m-1">EQTY/ETF
    
   </p>
    </div>
    <div class="vertical-line"></div>
    <div class="forex" class:tabbackcolor={check === 'seconddiv'} class:tabbgfront={check !== 'seconddiv'}  on:click={secondclick}>
<p class="m-1">Forex</p>
    </div>
    <div class="vertical-line"></div>
    <div class="crypto" class:tabbackcolor={check === 'thirddiv'} class:tabbgfront={check !== 'thirddiv'}  on:click={thirdclick}>
<p class="m-1">Crypto</p>
    </div>
    <div class="vertical-line"></div>
    <div class="col-2 m-2 mobileselect">
      <select bind:value={selectedOption} class="col-2 mobileselect">
        {#each options as option (option)}
          <option value={option} class="justify-content-center" >{option}</option>
        {/each}
        
      </select>
    </div>
    
  </div>
  
  <div class="col-10 mt-3  mx-auto">
    <div class="column">

    <div class="column  border border-2 rounded">
      
      <div class="d-flex flex-row  mx-3 my-2 col-12">
        <p class="col-2 mt-2 ">Rank</p>
        <p class="col-6  mt-2">User</p>
        <p class="col-3 mt-2">Score</p>

        
      
      
    </div>
    <div class="element-below-div border border-1">
      
  </div>
  <div class="d-flex flex-row  mx-3 my-2 col-12">
    <p class="col-2 mt-2 ">1</p>
    <p class="col-6  mt-2">alexpxl31</p>
    <p class="col-3 mt-2">$387.78 trediclion</p>
</div>
<div class="element-below-div border border-1">
      
</div>
<div class="d-flex flex-row  mx-3 my-2 col-12 ">
  <p class="col-2 mt-2 ">1</p>
  <p class="col-6  mt-2">alexpxl31</p>
  <p class="col-3 mt-2">$387.78 trediclion</p>

  


</div>
<div class="element-below-div border border-1">
      
</div>
<div class="d-flex flex-row  mx-3 my-2 col-12">
<p class="col-2 mt-2 ">1</p>
<p class="col-6  mt-2">alexpxl31</p>
<p class="col-3 mt-2">$387.78 trediclion</p>




</div>
<div class="element-below-div border border-1">
      
</div>
<div class="d-flex flex-row  mx-3 my-2 col-12">
<p class="col-2 mt-2 ">1</p>
<p class="col-6  mt-2">alexpxl31</p>
<p class="col-3 mt-2">$3  87.78 trediclion</p>




</div>
    </div>
    <nav aria-label="Page navigation example">
      <ul class="pagination mt-4 justify-content-center">
        <li class="page-item"><a class="page-link" href="#">Previous</a></li>
        <li class="page-item"><a class="page-link" href="#">1</a></li>
        <li class="page-item"><a class="page-link" href="#">2</a></li>
        <li class="page-item"><a class="page-link" href="#">3</a></li>
        <li class="page-item"><a class="page-link" href="#">Next</a></li>
      </ul>
    </nav>
    </div>


  </div>
</div>

{:else if screenWidth < 1024}
<!-- Tablet layout -->

<div class="column">
  <nav class="navbar navbar-expand-lg navbar-light bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand text-white" href="#">ChartGame</a>
      <button class="navbar-toggler bg-white" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Features</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Pricing</a>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              Dropdown link
            </a>
            <ul class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
              <li><a class="dropdown-item" href="#">Action</a></li>
              <li><a class="dropdown-item" href="#">Another action</a></li>
              <li><a class="dropdown-item" href="#">Something else here</a></li>
            </ul>
          </li>
        </ul>
      </div>
    </div>
  </nav>
  <div class="col-11 mt-5  mx-auto d-flex flex-row  border border-2 rounded">
    <div class="col-3 text-left" class:tabbackcolor={check === 'firstdiv'} class:tabbgfront={check !== 'firstdiv'}  on:click={firstclick}>
      <p class="mt-2 mx-2">EQY/ETF
        
      </p>
      
    </div>
    <div class="vertical-line"></div>
    <div class="col-3 text-left" class:tabbackcolor={check === 'seconddiv'} class:tabbgfront={check !== 'seconddiv'}  on:click={secondclick}>
      <p class="mt-2 mx-2" >Forex
        <span class="vertical-line"></span>
      </p>
      
    </div>
    
<div class="vertical-line"></div>
    <div class="col-3 text-left" class:tabbackcolor={check === 'thirddiv'} class:tabbgfront={check !== 'thirddiv'}  on:click={thirdclick}>
      <p class="mt-2 mx-2">Crypto
        

      </p>
      
    </div>
    <div class="vertical-line"></div>
    <select bind:value={selectedOption} class="col-2 selected" >
      {#each options as option (option)}
        <option value={option} class="justify-content-center" >{option}</option>
      {/each}
      
    </select>
    
  </div>
  
  <div class="col-11 mt-3  mx-auto">
    <div class="column">

    <div class="column  border border-2 rounded">
      
      <div class="d-flex flex-row  mx-3 my-2 col-12">
        <p class="col-3 mt-2 ">Rank</p>
        <p class="col-3  mt-2">User</p>
        <p class="col-3 mt-2">Score</p>

        
      
      
    </div>
    <div class="element-below-div border border-1">
      
  </div>
  <div class="d-flex flex-row  mx-3 my-2 col-12">
    <p class="col-3 mt-2 ">1</p>
    <p class="col-3  mt-2">alexpxl31</p>
    <p class="col-3 mt-2">$387.78 trediclion</p>
</div>
<div class="element-below-div border border-1">
      
</div>
<div class="d-flex flex-row  mx-3 my-2 col-12 ">
  <p class="col-3 mt-2 ">1</p>
  <p class="col-3  mt-2">alexpxl31</p>
  <p class="col-3 mt-2">$387.78 trediclion</p>

  


</div>
<div class="element-below-div border border-1">
      
</div>
<div class="d-flex flex-row  mx-3 my-2 col-12">
<p class="col-3 mt-2 ">1</p>
<p class="col-3  mt-2">alexpxl31</p>
<p class="col-3 mt-2">$387.78 trediclion</p>




</div>
<div class="element-below-div border border-1">
      
</div>
<div class="d-flex flex-row  mx-3 my-2 col-12">
<p class="col-3 mt-2 ">1</p>
<p class="col-3  mt-2">alexpxl31</p>
<p class="col-3 mt-2">$3  87.78 trediclion</p>




</div>
    </div>
    <nav aria-label="Page navigation example">
      <ul class="pagination mt-4 justify-content-center">
        <li class="page-item"><a class="page-link" href="#">Previous</a></li>
        <li class="page-item"><a class="page-link" href="#">1</a></li>
        <li class="page-item"><a class="page-link" href="#">2</a></li>
        <li class="page-item"><a class="page-link" href="#">3</a></li>
        <li class="page-item"><a class="page-link" href="#">Next</a></li>
      </ul>
    </nav>
    </div>


  </div>
</div>
{:else}
<!-- Laptop/desktop layout -->
<nav class="navbar navbar-expand-lg navbar-light bg-dark p-4 relative">
  <div class="container-fluid ">
    <a class="navbar-brand text-white" href="#">ChartGame</a>
    <button class="navbar-toggler bg-white" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
   
  </div>
 
                                
   <div class="absolute right-2 d-md-none d-lg-block">
<div class="d-flex flex-row mx-3 px-5 py-3">
<!-- First icon (e.g., a home icon) -->
<Fa icon={faHome}   class="mx-2 text-white " size="lg" />
<Fa icon={faList}  class="mx-2 text-white" size="lg" />
<Fa icon={faMessage}  class="mx-2 text-white" size="lg" />



</div>



   </div> 
   
</nav>
<div class="col-12 d-flex flex-row  px-5 ">
  
      <div class="col-5  m-2   px-3">
<div class="col-12  mt-5 border border-2 rounded">
  <div class="column">
  <div class="d-flex flex-row mx-auto justify-content-evenly ">
    <div class=" col-4  text-center child"  class:backcolor={check === 'firstdiv'} class:bgfront={check !== 'firstdiv'}  on:click={firstclick}>
      <p class="mt-2">Equities/Etf</p>
    </div>
    <div class="vertical-line bg-warning">

    </div>
    <div class="col-4 text-center child1"  class:backcolor={check === 'seconddiv'} class:bgfront={check !== 'seconddiv'}  on:click={secondclick}>
      
      <p class="mt-2">Forex</p>
    </div>
    <div class="vertical-line">

    </div>
    <div class="col-4 text-center child2"  class:backcolor={check === 'thirddiv'} class:bgfront={check !== 'thirddiv'}  on:click={thirdclick}>
      <p class="mt-2">Cryptocurrencies</p>
    </div>
  </div>
  
</div>
</div>
<div class="col-12  mt-3 border border-2 justify-content-center rounded ">
  <div class="networth">
    <p class="text-center pt-2">Net Worth ($)</p>
    <hr class="line">
</div>
<div  >
  <p class="text-center">Annual Compound Returns (%)</p>
  <hr class="line">
</div>
<div  >
  <p class="text-center">Day + Swing Trading (%)</p>
  <hr >
</div>
<div >
  <p class="text-center">Day Trading (%)</p>
  <hr>
</div>
<div >
  <p class="text-center">Swing Trading (%)</p>
  
</div>
</div>
         
      </div>
      <div class="col-6 mx-2 m-2 mt-5 px-3 py-1 mx-5">
        <div class="column">

        <div class="column  border border-2 rounded">
          
          <div class="d-flex flex-row  mx-3 my-2 col-12">
            <p class="col-2 mt-2 ">Rank</p>
            <p class="col-6  mt-2">User</p>
            <p class="col-3 mt-2">Score</p>

            
          
          
        </div>
        <div class="element-below-div border border-1">
          
      </div>
      <div class="d-flex flex-row  mx-3 my-2 col-12">
        <p class="col-2 mt-2 ">1</p>
        <p class="col-6  mt-2">alexpxl31</p>
        <p class="col-3 mt-2">$387.78 trediclion</p>
    </div>
    <div class="element-below-div border border-1">
          
    </div>
    <div class="d-flex flex-row  mx-3 my-2 col-12">
      <p class="col-2 mt-2 ">1</p>
      <p class="col-6  mt-2">alexpxl31</p>
      <p class="col-3 mt-2">$387.78 trediclion</p>

      
    
    
  </div>
  <div class="element-below-div border border-1">
          
  </div>
  <div class="d-flex flex-row  mx-3 my-2 col-12">
    <p class="col-2 mt-2 ">1</p>
    <p class="col-6  mt-2">alexpxl31</p>
    <p class="col-3 mt-2">$387.78 trediclion</p>

    
  
  
</div>
<div class="element-below-div border border-1">
          
</div>
<div class="d-flex flex-row  mx-3 my-2 col-12">
  <p class="col-2 mt-2 ">1</p>
  <p class="col-6  mt-2">alexpxl31</p>
  <p class="col-3 mt-2">$3  87.78 trediclion</p>

  


</div>
        </div>
        <nav aria-label="Page navigation example">
          <ul class="pagination mt-4 justify-content-center">
            <li class="page-item"><a class="page-link" href="#">Previous</a></li>
            <li class="page-item"><a class="page-link" href="#">1</a></li>
            <li class="page-item"><a class="page-link" href="#">2</a></li>
            <li class="page-item"><a class="page-link" href="#">3</a></li>
            <li class="page-item"><a class="page-link" href="#">Next</a></li>
          </ul>
        </nav>
        </div>


      </div>
      
      
</div>

{/if}