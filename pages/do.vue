<template>
    <div>
        <nav class="navbar navbar-expand-lg navbar-light small">
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
                    <a class="nav-link "  href="/">Deunion Reserve</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="/do">What we do</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/we">Who we Are</a>
                </li>
                <li class="nav-item ">
                    <a class="nav-link"  href="/contact">Contact Us</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/login">Client Login</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/signup">Client Registration</a>
                </li>
            </ul>
        </div>
        <div class="con2">

        </div>
        <div class="con">
            <h1>Corporate Banking</h1>
            <p>Deutsche Bank’s Corporate Bank addresses the needs of corporate clients, financial institutions, investors and issuers in three segments.
                In Corporate Treasury Services we provide corporate clients with liquidity management, foreign exchange, payment, trade finance and lending solutions.
                These services are orchestrated by a treasury coverage team that works closely with the Investment Bank to ensure cross-divisional alignment.
                Our Institutional Client Services provide financial institutions, investors and issuers with 
                institutional cash management, trust and agency solutions as well as securities services.
                In Germany, our Business Banking segment supports small businesses and self-employed business owners with payment and credit solutions as well as
                other banking services across our three brands Deutsche Bank, Postbank and the digital bank FYRST.
                At Deutsche Bank Corporate Bank we are passionate about our tradition as the Global Hausbank, and excited about shaping the future of financial services</p>
        </div>
        <div class="con">
            <h1>DWS</h1>
            <p>DWS Group GmbH & Co. KGaA (DWS) is one of the world's leading asset managers
                 with EUR 700bn of assets under management (as of 31 Dec 2017). Building on 
                 more than 60 years of experience and a reputation for excellence in Germany 
                 and across Europe, DWS has come to be recognized by clients globally as a 
                 trusted source for integrated investment solutions, stability and innovation 
                 across a full spectrum of investment disciplines.We offer individuals and institutions access to our strong investment capabilities across all major asset classes and solutions aligned to growth trends. Our diverse expertise in Active, Passive and Alternatives asset management – as well as our deep environmental, social and governance focus – complement each other when creating targeted solutions for our clients. Our expertise and on-the-ground-knowledge of our economists, research analysts and investment professionals are brought together in one consistent global CIO View, which guides our strategic investment approach.</p>
        </div>
        <div class="con">
            <h1>Investment Bank</h1>
            <p>The Investment Bank combines Deutsche Bank’s Fixed Income & Currencies, Origination & Advisory, as well as Deutsche Bank Research. It focuses on its traditional strengths in financing, advisory, fixed income and currencies. It provides strategic advice to corporate clients and includes a focused equity capital markets business, an equity and macro research capacity as well as a targeted equity sales force.

Fixed Income & Currencies brings together a top-ranked institutional sales force, world-class research with trading and structuring expertise across Foreign Exchange, Rates, Credit and Emerging Markets. The Fixed Income & Currencies business enables Deutsche Bank to respond to increasing automation, regulatory expectations and client demand for standardisation and transparency in execution across fixed income, currency and emerging markets.

Origination & Advisory aims to build long-term, trusted and mutually beneficial relationships with the major corporate clients, financial institutions, financial sponsors and sovereigns around the world.

Deutsche Bank Research is responsible for macro analysis and micro analysis within Deutsche Bank Group and acts as consultant for the bank, its clients and stakeholders. We analyse relevant trends for the bank in financial markets, the economy and society and highlight risks and opportunities. Deutsche Bank Research delivers high-quality, independent analysis and actively promotes public debate on economic, fiscal, labour market and social policy issues.</p>
        </div>
        <div class="con">
            <h1>Global Network</h1>
            <p>Against a backdrop of increasing globalization in the world economy, Deutsche Bank is very well-positioned, with significant regional diversification and substantial revenue streams from all the major regions of the world.

We have established strong bases in all major emerging markets, and therefore have good prospects for business growth in fast-growing economies, including the Asia Pacific region, Central and Eastern Europe, and Latin America.

In Europe, we are well placed to benefit from the aforementioned resilient conditions in our home market, Germany, and from continued strong levels of corporate activity in the euro zone.</p>
        </div>
        <div class="con">
            <h1>Corporate Social Responsibility</h1>
            <p>We want communities and economies to prosper. Around the world, we apply our global corporate social responsibility strategy to the most relevant local concerns.
We work together with like-minded partners towards this goal. Our people play their part too. We want to empower startups, non-profits and commercial businesses that create wider social good. Our Made for Good programme provides access to advice, support and networks to help them scale up. Wherever we do business we work to build stronger and more inclusive communities. We focus our efforts on the most disadvantaged through projects that deliver basic welfare, improve essential infrastructure and provide relief in emergencies.</p>
        </div>
        <footer-sections/>
    </div>
</template>
<style scoped>
@font-face {
    font-family: DMSans;
    src: url("/font/DMSans-Regular.ttf");
    }
    
    .con{
        margin-left: 5%;
        margin-right: 5%;
    }
    .con h1{
        color: #0272A2;
        margin-bottom: 2rem;
    }
    .grid{
      display: grid;
      grid-template-columns: 1fr 1fr;
    }
    .icons{
      text-decoration: underline;
      font-weight: bold;
    }
    .grid1{
      text-align: right;
      margin-top: 2px;
    }

    .con p{
        margin-bottom: 2rem;
    }
    .nav1{
        margin-top: 1rem;
    
    }
   
    .nav-item{
        margin-left: 3rem;
    }
    .active{
        border-bottom: 1px solid #dee2e6  !important ;
    }
    a{
        color: black;
    }
    .con2{
        background: url("/img/new/lu.jpg") center center/cover;
        height: 100vh;
        margin-bottom: 1rem;
    }
    .small{
      display: none;
    }

    @media(max-width:567px){
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
      
      border: 1px solid grey;
      font-size: 25px;
      display: inline;
      font-weight: bold;
      
     
    }
    .icon{
      font-size: 40px;
      color: black;
      border-radius: 50%;
      padding : 5px;
      margin-right: 10px;
      border: 1px solid grey;
    }
        .con{
        margin-left: 10px;
        margin-right: 10px;
    }
        .small{
      display:block
    }
    .big{
      display:none;
    }
    .active{
        border-bottom: none  !important ;
    }
    .nav-item{
        margin-left: 0rem;
        font-size: 17px;
    }
    .nav-link{
      color: black  !important;
    }
    .navbar-light .navbar-toggler {
    color: rgba(0, 0, 0, 0.5);
    border-color: rgba(0, 0, 0, 0.1);
    outline: none;
}
    }
</style>