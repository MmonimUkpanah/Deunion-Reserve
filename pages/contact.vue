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
                    <a class="nav-link" href="/do">What we do</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/we">Who we Are</a>
                </li>
                <li class="nav-item ">
                    <a class="nav-link active" aria-current="page" href="/contact">Contact Us</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/login">Client Login</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/signup">Client Registration</a>
                </li>
            </ul>
        </div>
        <div class="con">
            <h1>Contact</h1>
            <p>Your questions or comments are very important to us. For enquiries regarding online banking – including security topics, phishing, PIN/TAN numbers, banking terminals, lost or stolen credit cards, loans, savings etc. – please visit the relevant section of your local Private Bank website. You can send us an email for other topics.</p>
            <p>IMPORTANT NOTE: In order to maintain discretion, please do not email any confidential information such as account numbers. For your own security, since it is not possible to identify an email sender, Deutsche Bank cannot accept via email any orders for business transactions such as the opening of accounts, payment orders, trading orders, changes of address or the like. For such transactions, please contact the appropriate office. You can also find the address of all our locations worldwide at db.com/addresses. Send an email to deutsche.bank@db.com for other enquiries.</p>
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
    .con p{
        margin-bottom: 2rem;
    }
    .nav1{
        margin-top: 1rem;
        margin-bottom: 1rem;
    }
    .nav1{
        margin-top: 1rem;
        margin-bottom: 1rem;
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

    .nav-item{
        margin-left: 3rem;
    }
    .active{
        border-bottom: 1px solid #dee2e6  !important ;
    }
    a{
        color: black;
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