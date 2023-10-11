<script>


import Fa from 'svelte-fa'
  import { faFlag, faHamburger, faHome, faList, faMessage } from '@fortawesome/free-solid-svg-icons'
</script>
<style>
    
    @import 'bootstrap/dist/css/bootstrap.min.css';
    
    @import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

  .btnbg{
    background-color: #286090;
  }
.hzline{
    width:80vw;
    margin: auto;
}
.heading{
    background-color: #f5f5f5;
    height: auto;
    width: 100%;
}
.line{
  width: 90%;
  background-color: red;
  margin: auto;
}
.family{
  font-family: 'Poppins', sans-serif; 
}
.customborder{
  border-color:  grey;
}
.fontstyling{
  font-size: 14px;
  font-family: 'Poppins', sans-serif;
}
footer{
  background-color: black;
  height: auto;
  margin-top: 20px;
}
.fontdata{
  font-size: 24px;
}
.follower{
  font-size: 14px;
}
.para{
  font-size: 14px;
  line-height: 20px;
}
.parahead{
  font-family: 'Poppins', sans-serif; 
  font-weight: 500;
  font-size: 24px;
  color: #333333;
  line-height: 26px;
}
.news{
  font-style: normal;
  font-weight: 700;
  line-height: 20px;
  font-size: 14px;
  font-family: 'Poppins', sans-serif; 
}
</style>

<!-- for mobile devices -->
<div class="container d-md-none d-block">
  <div class="row">
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
    <div class="col-12 d-flex flex-row border mb-2 mt-3">
      <div class="col-6 ">
<h1>neh<h1>
      </div>
      <div class="col-6 ">
        <h2 class="family">name</h2>
        <div class="d-flex flex-row">

          <p class="family follower">Following<span>:0</span></p>
          <p class="mx-2 family follower">Followers<span>:0</span></p>
        </div>

   <p class="family follower">Equity Rank:<span class="mx-2">N/A</span></p>
              <p class="d-md-none d-lg-block family follower">Lifetime Games :<span class="mx-1">0</span></p>
              <!-- <p class="d-md-block d-lg-none w-[4%] family">Games in Lifetime:<span>0</span></p> -->
              <p class="family follower">Portfolio:<span class="mx-2">$300000</span></p>
      </div>
    </div>
    <div >
    <div class="row border">

      <div class="d-flex flex-row justify-content-center  gx-2 col-12 mt-1 ">
        <div class="d-flex flex-row col-3 mx-3">
        <input type="radio"/>
        <p class="mt-3 mx-2 follower family">Equities/Etf</p>
        </div>
        <div class="d-flex flex-row col-3 mx-3" >
          <input type="radio"/>
          <p class="mt-3 mx-2 follower family">Forex  </p>
          </div>
          <div class="d-flex flex-row col-4 mx-3">
            <input type="radio"/>
            <p class="mt-3 mx-2 follower family">Cryptocurrencis</p>
            </div>
            
           
        
      </div>
      <hr>
      <div class="d-flex flex-row col-12 border">
        <div class="d-flex flex-row justify-content-center  ">
          <button class=" btnbg m-2 py-2 px-2 text-white rounded border-0 follower family">Play DayTrader Simulation</button>
          <button class="btnbg m-2 py-2 px-2 text-white rounded border-0 follower family  ">Play SwingTrader Simulation</button>
      </div>
      </div>
    </div>
    <div class="d-flex flex-row px-5 mx-5">
      <div class="col-3">
         <div class="d-flex flex-row">
          <input type="checkbox" class="m-2"/>
          <p class="mt-2 follower family">practice</p>

         </div>
      </div>
    </div>
   <div class="col-12 border">
    <div class="heading bg-grey">
      <p class="py-2 text-sm px-2 fw-bold">Human Lifetime Net Worth (Equities/ETFs)</p>
      <hr>
    </div>
<div class="d-flex flex-row col-12 justify-content-center">
   <p class="col-2 family follower">Rank</p>
   <p class="col-2 family follower">User</p>
   <p class="col-3 family follower">Net Worth</p>
   <p class="col-2 family follower">ACR</p>
   
</div>
<div class="d-flex flex-row col-12 justify-content-center">
  <p class="col-2 family follower">1</p>
  <p class="col-2 family follower">User</p>
  <p class="col-3 family follower">$356.76 tredecilion</p>
  <p class="col-2 family follower">$356.76 </p>
  
</div>
   </div>
   <div class="col-12 mx-2  mt-4 mx-auto border   rounded customborder">
    <div class="heading bg-grey">
      <p class="py-2 text-sm px-2 fw-bold news">News</p>
      <hr>
    </div>
    <div class="d-flex flex-row justify-content-end">
         <p class="mx-4 my-1 follower family">01/12/2019</p>
         
    </div>
    <div class="mt-2">
      <h3 class="mx-3 fw-normal family">Emergency Maintainane and update</h3>
      <p class="mx-3 mt-4 fontstyling text-sm para">ChartGame will be down on Sunday, January 13th between 7:30pm and 9:30pm PST for an update. All active games will be deleted for this update so please finish your game before this update.
      </p>

  </div>
  <hr>
  <div class="d-flex flex-row justify-content-end">
    <p class="mx-4 my-1 follower family">01/12/2019</p>
    
</div>
  <div class="mt-2">
    <h3 class="mx-3 fw-normal family">Emergency Maintainane and update</h3>
    <p class="mx-3 mt-4 fontstyling para">ChartGame will be down on Sunday, January 13th between 7:30pm and 9:30pm PST for an update. All active games will be deleted for this update so please finish your game before this update.
    </p>

</div>
<hr>
<div class="d-flex flex-row justify-content-end">
  <p class="mx-4 my-1 follower family">01/12/2019</p>
  
</div>
<div class="mt-2">
  <h3 class="mx-3 fw-normal parahead">Emergency Maintainane and update</h3>
  <p class="mx-3 mt-4 fontstyling para">ChartGame will be down on Sunday, January 13th between 7:30pm and 9:30pm PST for an update. All active games will be deleted for this update so please finish your game before this update.
  </p>

</div>
  </div>
    </div>
  </div>

</div>
<div class="container-fluid   d-none d-md-block">
    
    <div class="row checkagain">
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
    <div class="row mt-5">
        <div class="col-12 d-flex flex-row gx-2">
            <div class="col-5 border mx-auto rounded customborder ">
              <div class="d-flex flex-row mt-3  h-full">
           <div class="col-6 bg-danger mx-2 ">

           </div>
           <div class="col-6">
              <h2 class="family fontdata  ">Name</h2>
              <div class="d-flex flex-row d-md-none d-lg-flex">
              <p class="family follower">Following<span>:0</span></p>
              <p class="mx-2 family follower">Followers<span>:0</span></p>
              </div>

              <div class="column d-md-block d-lg-none ">
                <p class="family follower">Following<span>:0</span></p>
                <p class="family follower">Followers<span>:0</span></p>
              </div>
              <p class="family follower">Equity Rank:<span class="mx-2">N/A</span></p>
              <p class="d-md-none d-lg-block family follower">Lifetime games :<span class="mx-1">0</span></p>
              <div class="d-flex flex-row">
                <div class="column">
                 <p class="family d-md-block d-lg-none follower">Lifetimegames:</p>

                </div>
                <p  class="px-1 d-lg-none d-md-block">0</p>
                
              </div>
              
              <p class="follower family">Portfolio:<span class="mx-1 family follower  ">$300000</span></p>
            
           </div>
              </div>
            </div>
            <div class="col-6 mx-2 mx-auto border  px-2 rounded customborder">
                <div class="column justify-content-center">
                <div class="d-flex flex-row justify-content-center  gx-2 col-12 mt-1 d-md-none d-lg-flex">
                  <div class="d-flex flex-row col-3 col-md-2 ">
                  <input type="radio"/>
                  <p class="mt-3 mx-1 family">Equities/Etf</p>
                  </div>
                  <div class="d-flex flex-row col-3 mx-5 col-md-2">
                    <input type="radio"/>
                    <p class="mt-3 mx-2 family">Forex</p>
                    </div>
                    <div class="d-flex flex-row col-3 col-md-2">
                      <input type="radio"/>
                      <p class="mt-3 mx-1 family">Cryptocurrencis</p>
                      </div>
                  
                </div>
                <!-- for devices medium -->
                <div class="d-flex flex-row justify-content-center  gx-2 col-12 mt-1 d-md-block d-lg-none">
                  <div class="d-flex flex-row justify-content-center">
                   <div class="d-flex flex-row mx-3">
                    <input type="radio"/>
                    <p class="pt-2 px-1  mt-2 family follower">Equities/Etf</p>
                   </div>
                   <div class="d-flex flex-row mx-3">
                    <input type="radio"/>
                    <p class="pt-2 px-1  mt-2 family follower">Forex</p>
                   </div>
                   <div class="d-flex flex-row mx-3">
                    <input type="radio"/>
                    <p class="pt-2 px-1 mt- mt-2 family follower">Cryptocurencies</p>
                   </div>
                  </div>
                  
                </div>
                <hr >
                <div class="d-flex flex-row justify-content-center">
                    <button class=" btnbg  m-2 py-2 text-white rounded border-0 follower family">Play DayTrader Simulation</button>
                    <button class="btnbg m-2  py-2 text-white rounded border-0 follower family">Play SwingTrader Simulation</button>
                </div>
                <hr>
                <div class="d-flex flex-row px-5 mx-5">
                    <div class="col-3">
                       <div class="d-flex flex-row">
                        <input type="checkbox" class="m-2"/>
                        <p class="mt-2 family">practice</p>

                       </div>
                    </div>
                  
                </div>
                
                </div>
            </div>
        </div>
    </div>
    <div class="row mt-5 ">
      <div class="col-12 d-flex flex-row ">
          <div class="col-5 border mx-auto rounded customborder">
            <div class="heading">
              <p class="fw-bolder text-sm text-left py-3 mx-2 family">Human Lifetime Net Worth (Equities/ETFs)</p>
              
             </div>
             <div class="row ">
             <div class="col-12 d-flex flex-row mx-auto ">
              <div class="col-2 ">
                <p class="text-center text-md-center  family follower">Rank</p>
              </div>
               <div class="col-3">
                   <p class="text-left text-md-center family follower">User</p>
               </div>
               <div class="col-4">
                   <p class="text-left text-md-center family follower">Net Worth</p>
               </div>
               <div class="col-3">
                  <p class="text-center text-md-center family follower">ACR</p>
               </div>
             </div>
             <div class="col-12 d-flex flex-row mx-auto">
              <div class="col-2 ">
                <p class="text-center family follower">1</p>
              </div>
               <div class="col-3">
                   <p class="text-left text-md-center family follower">alexpixe31</p>
               </div>
               <div class="col-4">
                   <p class="text-md-center family follower">$356.76 tredecilion</p>
               </div>
               <div class="col-3">
                  <p class="text-center family follower">364.5%</p>
               </div>
             </div>
             
            </div>
          </div>
          <div class="col-6 mx-2 mx-auto border   rounded customborder">
            <div class="heading bg-grey">
            <p class="py-2 text-sm px-2 fw-bold  news">News</p>
            <hr>
          </div>
          <div class="d-flex flex-row justify-content-end">
            <p class="mx-4 my-1 follower">01/12/2019</p>
            
        </div>
            <div class="mt-2">
              <h3 class="mx-3 fw-normal parahead">Emergency Maintainane and update</h3>
              <p class="mx-3 mt-4 fontstyling para">ChartGame will be down on Sunday, January 13th between 7:30pm and 9:30pm PST for an update. All active games will be deleted for this update so please finish your game before this update.
              </p>

          </div>
          <hr>
          <div class="d-flex flex-row justify-content-end">
            <p class="mx-4 my-1">01/12/2019</p>
            
       </div>
          <div class="mt-2">
            <h3 class="mx-3 fw-normal parahead">Emergency Maintainane and update</h3>
            <p class="mx-3 mt-4 fontstyling para">ChartGame will be down on Sunday, January 13th between 7:30pm and 9:30pm PST for an update. All active games will be deleted for this update so please finish your game before this update.
            </p>

        </div>
        <hr>
        <div class="d-flex flex-row justify-content-end">
          <p class="mx-4 my-1">01/12/2019</p>
          
     </div>
        <div class="mt-2">
          <h3 class="mx-3 fw-normal parahead">Emergency Maintainane and update</h3>
          <p class="mx-3 mt-4 fontstyling para">ChartGame will be down on Sunday, January 13th between 7:30pm and 9:30pm PST for an update. All active games will be deleted for this update so please finish your game before this update.
          </p>

      </div>
          </div>
      </div>
  </div>
    
</div>
</div>
<footer>
<p class="text-center text-white py-5">User Agreement | privacy policy</p>
</footer>
