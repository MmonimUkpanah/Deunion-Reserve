<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-light small fixed-top">
        <div class="container-fluid">
          <a class="navbar-brand" href="/">Deunion Reserve</a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo02" aria-controls="navbarTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item ic">
               <a href="/"><h1>DE</h1></a> <font-awesome-icon :icon="['fas', 'share-alt']" class="icon" /> <font-awesome-icon :icon="['fas', 'link']" class="icon" /> <font-awesome-icon :icon="['fas', 'envelope']" class="icon" />
              </li>
              <li class="nav-item grid">
                <a class="nav-link icons" href="/">Deunion Reserve </a><span class="grid1"><font-awesome-icon :icon="['fas', 'home']" class="" /></span>
              </li>
              <li class="nav-item grid">
                <a class="nav-link active" aria-current="page" href="/do">What we do </a><span class="grid1"><font-awesome-icon :icon="['fas', 'chevron-circle-right']" class="ico" /></span>
              </li>
              <li class="nav-item grid">
                <a class="nav-link" href="/we">Who we are </a><span class="grid1"><font-awesome-icon :icon="['fas', 'chevron-circle-right']"  /></span>
              </li>
              <li class="nav-item grid">
                <a class="nav-link" href="/contact">Contact Us </a><span class="grid1"><font-awesome-icon :icon="['fas', 'chevron-circle-right']"  /></span>
              </li>
              <li class="nav-item ">
                <a class="nav-link icons" href="/login">Client Login</a>
              </li>
              <li class="nav-item">
                <a class="nav-link icons" href="/signup">Client Registration</a>
              </li>
              
            </ul>
            
          </div>
        </div>
      </nav>
    <div class="nav1 big">
            <ul class="nav nav-tabs">
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="#">Deunion Reserve</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/do">What we do</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/we">Who we Are</a>
                </li>
                <li class="nav-item ">
                    <a class="nav-link" href="/contact">Contact Us</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/login">Client Login</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/signup">Client Registration</a>
                </li>
            </ul>
        </div>
   <!-- <div class="one">
     <VueSlickCarousel v-bind="settings">
      <div class="two1">
        <div class="two12">
          <h1>Deutsche Bank reports on target delivery and progress on sustainability in 2020</h1>
        </div>
        
      </div>
      <div class="two2">
        <div class="two12">
          <h1>Germany in the next decade: Ambition and potential</h1>
        </div>
        
      </div>
      <div class="two3">
        <div class="two12">
          <h1>Deutshe Bank reports &#65505;1.6 billion profit before tax in the first quarter of 2021</h1>
        </div>
        
      </div>
      <div class="two6">
        <div class="two12">
          <h1>Asset-as-a-service</h1>
          <p>The transformation from Capex to Opex - a step further towards Industry 4.0</p>
        </div>
        
      </div>
      <div class="two5">
        <div class="two12">
          <p>What's next - Responsible Growth</p>
          <h1>Togs from Trash</h1>
          <p>Italian company Aquafil produces Nylon from waste - and maskes the fashion industry more sustainable</p>
        </div>
        
      </div>
      
    </VueSlickCarousel>
   </div> -->
   <!-- <div class="carousel big">
     <b-carousel
    id="carousel-fade"
    style="text-shadow: 0px 0px 2px #000"
    fade
    indicators
    img-width="1024"
    img-height="50vh"
  >
    
    <b-carousel-slide class="two1">
    <div class="cap">
      <h1>Deutsche Bank reports on target delivery and progress on sustainability in 2020</h1>
    </div>
        
       
      </b-carousel-slide>
      <b-carousel-slide class="two2">
       <div class="cap">
          <h1>Asset-as-a-service</h1>
          <p>The transformation from Capex to Opex - a step further towards Industry 4.0</p>
       </div>
      </b-carousel-slide>
       <b-carousel-slide class="two3">
       <div class="cap">
         
          <h1>Germany in the next decade: Ambition and potential</h1>

       </div>
      </b-carousel-slide>
      <b-carousel-slide class="two4">
       <div class="cap">
         
          <h1>Deutshe Bank reports &#65505;1.6 billion profit before tax in the first quarter of 2021</h1>

       </div>
      </b-carousel-slide>
      <b-carousel-slide class="two5">
       <div class="cap">
         <p>What's next - Responsible Growth</p>
          <h1>Togs from Trash</h1>
          <p>Italian company Aquafil produces Nylon from waste - and maskes the fashion industry more sustainable</p>
         

       </div>
      </b-carousel-slide>
      
  </b-carousel>
   </div> -->
   <div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active two1">
      <div class="cap">
      <h1>Deutsche Bank reports on target delivery and progress on sustainability in 2020</h1>
    </div>
    </div>
    <div class="carousel-item two2">
      <div class="cap">
          <h1>Asset-as-a-service</h1>
          <p>The transformation from Capex to Opex - a step further towards Industry 4.0</p>
       </div>
    </div>
    <div class="carousel-item two3">
      <div class="cap">
        <h1>Germany in the next decade: Ambition and potential</h1>
      </div>
       
    </div>
    <div class="carousel-item two4">
      <div class="cap">
         <h1>Deutshe Bank reports &#65505;1.6 billion profit before tax in the first quarter of 2021</h1>
      </div>
     
    </div>
    <div class="carousel-item two5">
      <div class="cap">
        <p>What's next - Responsible Growth</p>
          <h1>Togs from Trash</h1>
          <p>Italian company Aquafil produces Nylon from waste - and maskes the fashion industry more sustainable</p>
      </div>
       
    </div>
  </div>
</div>
   <div class="three">
     <div class="three1">
       <img src="/img/new/stefan.jpg" alt="">
       <div class="three2">
         <p>News | April 30, 2021</p>
         <h5>Virtual AGM 2.0: Deutsche Bank is at the forefront</h5>
       </div>
     </div>
     <div class="three1">
       <img src="/img/new/chris.jpg" alt="">
      <div class="three2">
         <p>News | April 28, 2021</p>
         <h5>A message from Christian Sewing on Q1 results 2021</h5>
       </div>
     </div>
     <div class="three1">
       <img src="/img/new/ann.jpg" alt="">
      <div class="three2">
         <p>Media Release | April 30, 2021</p>
         <h5>Deutsche Bank reports &#65505;1.6 billion profit before tax in the first quarter of 2021 </h5>
       </div>
     </div>
     <div class="three1">
       <img src="/img/new/wind.jpg" alt="">
      <div class="three2">
         <p>Media Release | April 30, 2021</p>
         <h5>Providing sustainable trade financing to Vestas for wind turbines in Australia </h5>
       </div>
     </div>
   </div>
   <div class="four">
     <div class="four1">
       <VueSlickCarousel v-bind="set">
        <div class="four2">
          <img src="/img/new/db.jpg" alt="">
          <h4>dbSustainability</h4>
          <p>Supporting clients with ESG integration into investment processes</p>
        </div>
        <div class="four2">
          <img src="/img/new/flow.jpg" alt="">
          <h4>Flow</h4>
          <p>Thought leadership platform for corporate clients</p>
        </div>
        <div class="four2">
          <img src="/img/new/mate.jpg" alt="">
          <h4>Climate Statement</h4>
          <p>Deutsche Bank's numerous climate-related activities</p>
        </div>
        <div class="four2">
          <img src="/img/new/sars.jpg" alt="">
          <h4>Corona Crisis</h4>
          <p>Recent research about the pandemic and it's consequences</p>
        </div>
        <div class="four2">
          <img src="/img/new/code.jpg" alt="">
          <h4>Code of conduct</h4>
          <p>Deutsche Bank's standards of behaviour and conduct</p>
        </div>
        <div class="four2">
          <img src="/img/new/bank.jpg" alt="">
          <h4>Strategy</h4>
          <p>Deutsche Bank is moving into phase 3 of it's transformation</p>
        </div>
      
      </VueSlickCarousel>
     </div>
   </div>
   <div class="three">
     <div class="three1">
       <img src="/img/new/cb.jpg" alt="">
       <div class="three2">
         <p>Flow Article | April 30, 2021</p>
         <h5>Recharging personal transportation</h5>
         <p>More than a decade after Tesla launched the first mass-produced electric vehicle, the end of the road is approaching
           for the conventional internal combustion engine. Flow's Graham Buck and Janet Du CHenne report on how an all-electric future
           is to be achieved.
         </p>
       </div>
     </div>
     <div class="three1">
       <img src="/img/new/more.jpg" alt="">
      <div class="three2">
         <p>Flow article | April 28, 2021</p>
         <h5>Doing more with less</h5>
        <p>More than a year on since the onset of Covid-19, the pandemic has made centralisation a top priority for many corporate treasurers and strengthened the case 
          for using an in-house bank, reports flow's Graham Buck.
        </p>
       </div>
     </div>
     <div class="three1">
       <img src="/img/new/co.jpg" alt="">
      <div class="three2">
         <p>Flow article | April 30, 2021</p>
         <h5>Covid-19: Towards herd immunity? </h5>
        <p>Production shortfalls, political wrangling, safety concerns and vaccine hesitancy have created barriers on the road to normalcy, but overall roll-out of injections is nonetheless advancing steadily, reports flow's Graham Buck and Clarissa Dann.</p>
       </div>
     </div>
     <div class="three1">
       <img src="/img/new/and.jpg" alt="">
      <div class="three2">
         <p>Flow Article | April 30, 2021</p>
         <h5>Sustainability and supply chains </h5>
        <p>While ESG principles and alignment start at home, they mst carry through to supply chains, explains Deutsche Bank's Anil Walia and Bjoern Goedecke in BCR's World Supply Chain Finance Report 2021.</p>
       </div>
     </div>
   </div>
   <div class="five">
     <div class="five1">
       <h4>Graduate? Professional?</h4>
       <p>The world is changing, and so are we. This is more than banking.</p>
      <p>Opportunities for agile minds start here</p>
     </div>
     <div class="five2">
        <h4>Financial releases, reports and calendar</h4>
        <p>Consult our financial reporting and events or read our creditor information</p>
     </div>
     <div class="five3">
     <h4>Share price (EUR)</h4>
      <div class="five31">
        <div class="five33">
          <h3>11.32</h3>
        </div>
        <div class="five32">
          <p>0.28</p>
          <h5>EUR</h5>
        </div>
      </div>
      <p>Intraday (Xetra, May 5, 16:36)</p>
      <p>Relative Change: 2.54%</p>
      <p>High: 11.42 EUR</p>
      <p>Low: 11.21 EUR</p>
     </div>
   </div>
      
    <footer-sections/>
  </div>
</template>



<script>

  import VueSlickCarousel from 'vue-slick-carousel'
  import 'vue-slick-carousel/dist/vue-slick-carousel.css'
  // optional style for arrows & dots
  import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
  

export default {
  components: { VueSlickCarousel, },
    data(){
        return{
           settings: {
                      "arrows": false,
                      "dots": false,
                      "infinite": true,
                      "slidesToShow": 1,
                      "slidesToScroll": 1,
                      "autoplay": true,
                      "speed": 10000,
                      "autoplaySpeed": 10000,
                      "cssEase": "linear",
                      "pauseOnDotsHover": true,
                      "pauseOnFocus": true,
                      "pauseOnHover": true },
              set: {
                    "dots": true,
                    "focusOnSelect": true,
                    "infinite": true,
                    "speed": 500,
                    "slidesToShow": 1,
                    "slidesToScroll": 1,
                    "touchThreshold": 5,
                    "responsive": [
    {
      "breakpoint": 1024,
      "settings": {
        "slidesToShow": 3,
        "slidesToScroll": 3,
        "infinite": true,
        "dots": true
      }
    },
    {
      "breakpoint": 600,
      "settings": {
        "slidesToShow": 2,
        "slidesToScroll": 2,
        "initialSlide": 2
      }
    },
    {
      "breakpoint": 480,
      "settings": {
        "slidesToShow": 1,
        "slidesToScroll": 1,
        "arrows": false,
        "autoplay": true,
        "speed": 10000,
        "autoplaySpeed": 10000,
        "cssEase": "linear",
        "pauseOnDotsHover": true,
        "pauseOnFocus": true,
        "pauseOnHover": true
      }
    },
  ]
                  } ,
                   slide: 0,
        sliding: null,   
            
        }
    },
    methods:{
        
    }
}
</script>





<style >
@font-face {
    font-family: DMSans;
    src: url("/font/DMSans-Regular.ttf");
    }
    *{
        font-family: 'DM Sans', sans-serif  !important;
        padding: 0;
        margin: 0;
    }
    .slick-prev:before, .slick-next:before {
    font-family: 'slick';
    font-size: 20px;
    line-height: 1;
    opacity: 0.75;
    color: black;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}
    
    .one{
      width:100%;
      color: rgb(172, 107, 107);
    }
    .two{
      width: 100%  !important;
    }
    
    .two1{
      background: linear-gradient(
            to right,
            rgba(0, 4, 23, 0.58),
            rgba(0, 4, 23, 0.58)
        ),url(/img/new/bank1.jpe) center center/cover;
    height: 70vh;
    }
    .cap{
      padding-top: 3rem;
      padding-left: 5%;
      padding-right: 5%;;
      text-align: left;
      color: white;
    }
    .cap h1{
      font-size: 70px;
    }
    .cap p{
      font-size: 30px;
    }
    .two2{
      background: linear-gradient(
            to right,
            rgba(0, 4, 23, 0.58),
            rgba(0, 4, 23, 0.58)
        ),url(/img/new/bank2.jpe) center center/cover;
        height: 70vh;
    
    }
    .small{
      display: none;
    }
    
    .two3{
      background: linear-gradient(
            to right,
            rgba(0, 4, 23, 0.58),
            rgba(0, 4, 23, 0.58)
        ),url(/img/new/bank3.jpe) center center/cover;
    height: 70vh;
    }
    .two4{
      background: linear-gradient(
            to right,
            rgba(0, 4, 23, 0.58),
            rgba(0, 4, 23, 0.58)
        ),url(/img/new/germany.jpe) center center/cover;
    height: 70vh;
    }
    .two5{
      background: linear-gradient(
            to right,
            rgba(0, 4, 23, 0.58),
            rgba(0, 4, 23, 0.58)
        ),url(/img/new/clothes.jpe) center center/cover;
    height: 70vh;
    }
    .two6{
      background: linear-gradient(
            to right,
            rgba(0, 4, 23, 0.58),
            rgba(0, 4, 23, 0.58)
        ),url(/img/new/sedan.jpe) center center/cover;
    height: 70vh;
    }
    .two12{
      margin-left: 10%;
      margin-right: 10%;
      padding-top: 8rem;
    }
    .two12 h1{
      font-size: 65px;
      margin-bottom: 0.5rem;
    }
    .two12 p{
      font-size: 20px;
      margin-bottom: 0.5rem;
    }
    .three{
      margin-top: 4rem;
      margin-left: 5%;
      margin-right: 5%;
      display: grid;
      grid-template-columns: 1fr 1fr 1fr 1fr;
      grid-column-gap: 1rem;
    }
    .three1{
      box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    }
    .three1 img{
      width: 100%;
      height: 210px;
    }
    .three2{
      padding:1rem 
    }
    .three2 p{
      color: #425563;
      margin-bottom: 0.5rem;
    }
    .four{
      margin-top: 4rem;
      background: #e5f5fb;
    }
    .four1{
      padding-left: 6%;
      padding-right: 6%;
      padding-top: 2rem;
      padding-bottom: 2rem;
    }
    .four2 img{
      width: 97%;
      height: 210px;
    }
    .four2{
      text-align: center;
      margin-right: 5rem;
    }
    .four2 h4{
      padding-top: 0.5rem;
    }
    .five{
      margin-top: 4rem;
      margin-left: 5%;
      margin-right: 5%;
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      grid-gap: 2rem;
    }
    .five1{
      background: purple;
      color: white;
      padding: 3rem 2rem;
    }
    .five1 h4{
      font-size: 35px;
      margin-bottom: 1rem;
    }
    .five1 p{
      font-size: 20px;
    }
    .five2{
      background: #0272A2;
      color: white;
      padding: 3rem 2rem;
    }
    .five2 h4{
      font-size: 35px;
      margin-bottom: 1rem;
    }
    .five2 p{
      font-size: 20px;
    }
    .five3{
      background: #f3f4f5;
      color: black;
      padding: 3rem 2rem;
    }
    .five3 h4{
      font-size: 35px;
      margin-bottom: 1rem;
    }
    .five3 p{
      font-size: 20px;
    }
    .five31{
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
    }
    .five33 h3{
      font-size: 55px;
      color: #0272A2;
    }
    .five32 p{
      color: darkgreen;
    }
    .five32 h5{
      color: black;
    }
    .active{
        border-bottom: 1px solid #dee2e6  !important ;
    }
    a{
        color: black;
    }
    .nav1{
        margin-top: 1rem;
    }
    .nav-item{
        margin-left: 3rem;
    }
    .nav-link{
      color: black  !important;
    }
    


    .grid{
      display: grid;
      grid-template-columns: 1fr 1fr;
    }
    .grid1{
      text-align: right;
      margin-top: 7px;
    }



    @media(max-width:567px){
      .cap{
         padding-top: 0rem;
      margin-top: 7rem;
      text-align: center;
      color: white;
      padding-left: 10px;
      padding-right: 10px;
    }
    .cap h1{
      font-size: 40px;
    }
    .cap p{
      font-size: 20px;
    }
      .ic{
      display: grid;
      grid-template-columns: 1fr 1fr 1fr 1fr  ;
     
     margin-top: 1rem;
     margin-bottom: 1rem;
    }
    .ic h1{
      color: black;
      border-radius: 50%;
      width:60%;
      padding: 5px;
      margin-right: 10px;
      margin-top: 3px;
      border: 1px solid grey;
      font-size: 25px;
     
      font-weight: bolder;
      
     
    }
   
    .icons{
      text-decoration: underline;
      font-weight: bold;
    }
    .icon{
      font-size: 45px;
      color: black;
      border-radius: 50%;
      padding : 10px;
      margin-right: 10px;
      border: 1px solid grey;
    }
      .active{
        border-bottom: none  !important ;
    }
      .two12{
      margin-left: 10px;
      margin-right: 10px;
      padding-top: 4rem;
    }
    .two12 h1{
      font-size: 50px;
      margin-bottom: 0.5rem;
    }
    .two12 p{
      font-size: 20px;
      margin-bottom: 0.5rem;
    }
    .three{
      margin-top: 4rem;
      margin-left: 10px;
      margin-right: 10px;
      display: grid;
      grid-template-columns: 1fr ;
      grid-gap: 1rem;
    }
    .three1 img{
      width: 100%;
      height: 210px;
    }
    .five{
      margin-top: 4rem;
      margin-left: 10px;
      margin-right: 10px;
      display: grid;
      grid-template-columns: 1fr;
      grid-gap: 2rem;
    }
    .five31{
      display: grid;
      grid-gap: 10px;
      grid-template-columns: 1fr 1fr 1fr;
    }
    .small{
      display:block;
      background: white;
    }
    .carousel{
      margin-top: 4rem;
    }
    .big{
      display:none;
    }
    .nav1{
        margin-top: 1rem;
    }
    .nav-item{
        margin-left: 0rem;
        font-size: 17px;
    }
    .navbar-light .navbar-toggler {
    color: rgba(0, 0, 0, 0.5);
    border-color: rgba(0, 0, 0, 0.1);
    outline: none;
}
  
    }
    
  





  

  
</style>