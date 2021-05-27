<template>
    <div>
        <nav class="navbar navbar-expand-lg navbar-light small">
        <div class="container-fluid">
          <a class="navbar-brand" href="/">SIMPLE BANK OF AMERICA</a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo02" aria-controls="navbarTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="/do">What we do</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="/we">Who we are</a>
              </li>
              <li class="nav-item">
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
        </div>
      </nav>
    <div class="nav1 big">
      <nav class="nav">
        
      <a class="nav-link active" aria-current="page" href="#"><img src="/img/new/simp.png" alt="" width="200rem" ></a>
      <a class="nav-link" href="#" style="padding-top:1.5rem;font-weight:600;border-bottom: 2.5px solid #0272A2">Activity</a>
      <a class="nav-link" href="#" style="padding-top:1.5rem">Expenses</a>
      <a class="nav-link" href="#" style="padding-top:1.5rem">Goals</a>
      <a class="nav-link" href="#" style="padding-top:1.5rem">CDs</a>

      <ul class="nav justify-content-end">
        <li class="nav-item dropdown" style="padding-top:1rem">
          <a class="nav-link dropdown-toggle" data-bs-toggle="dropdown" href="#" role="button" aria-expanded="false"><font-awesome-icon class="icon" :icon="['fas', 'gift']"/>  Refer a friend</a>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">Action</a></li>
            <li><a class="dropdown-item" href="#">Another action</a></li>
            <li><a class="dropdown-item" href="#">Something else here</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item" href="#">Separated link</a></li>
          </ul>
        </li>
        <li class="nav-item dropdown" style="padding-top:0.5rem">
          <a class="nav-link dropdown-toggle" data-bs-toggle="dropdown" href="#" role="button" aria-expanded="false"><p class="j">J</p> Joseph Grimaldi</a>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">Action</a></li>
            <li><a class="dropdown-item" href="#">Another action</a></li>
            <li><a class="dropdown-item" href="#">Something else here</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item" href="#">Separated link</a></li>
          </ul>
        </li>
        <li class="nav-item" style="padding-top:1rem">
          <a class="nav-link" href="#"><font-awesome-icon class="icono" :icon="['fas', 'question-circle']"/> </a>
        </li>
      </ul>
      
      
      
    </nav>
            <!-- <ul class="nav nav-tabs">
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="#"><img src="/img/new/simp.png" alt="" width="200rem" ></a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/do">Activity</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/we">Expenses</a>
                </li>
                <li class="nav-item ">
                    <a class="nav-link" href="/contact">Goals</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/login">CDs</a>
                </li>
                
            </ul>  -->
        </div>
        <div class="ba">
          <div class="ba1">
            <h1>$110,000</h1>
            <p>$110,000 available balance - $0.00 in scheduled activities - $0.00 in Expenses - $0.00 in Goals</p>
          </div>
          <div class="ba2">
            <h3>Protected Goals</h3>
            <p>Start a Savings Goal Today!</p>
          </div>
          <div class="ba2">
            <h3>CDs</h3>
            <p>Open a CD today!</p>
          </div>
            
        </div>
        <div class="search">
          <input type="search" placeholder="Search activity..."><button class="sb">Search</button><button class="mo">Move Money</button>
        </div>
        <div class="ta">
          <div class="table-responsive">
            <table class="table  table-striped table-hover">
                                            <thead>
                                                <tr>
                                                
                                                <th scope="col">Date</th>
                                                <th scope="col">Reference Number</th>
                                              
                                                <th scope="col">Amount</th>
                                                                                
                                                </tr>
                                            </thead>
                                            <tbody>
                                                <tr>
                                                  <td scope="row">24/05/2021</td>
                                                  <td>987654678723</td>
                                                  
                                                  <td>-$25,000</td>                                         
                                                </tr>
                                                <tr>
                                                  <td scope="row">24/05/2021</td>
                                                  <td>987654678765</td>
                                                  
                                                  <td>+$50,000</td>                                         
                                                </tr>
                                                <tr>
                                                  <td scope="row">22/05/2021</td>
                                                  <td>987654678729</td>
                                                  
                                                  <td>-$30,000</td>                                         
                                                </tr>
                                                <tr>
                                                  <td scope="row">20/05/2021</td>
                                                  <td>987654678794</td>
                                                  
                                                  <td>+$30,000</td>                                         
                                                </tr>
                                                <tr>
                                                  <td scope="row">19/05/2021</td>
                                                  <td>987654678743</td>
                                                  
                                                  <td>-$15,000</td>                                         
                                                </tr>
                                                <tr>
                                                  <td scope="row">15/05/2021</td>
                                                  <td>987654678726</td>
                                                 
                                                  <td>+$50,000</td>                                         
                                                </tr>
                                                <tr>
                                                  <td scope="row">14/05/2021</td>
                                                  <td>987654678723</td>
                                                  
                                                  <td>-$30,000</td>                                         
                                                </tr>
                                                <tr>
                                                  <td scope="row">10/05/2021</td>
                                                  <td>987654678729</td>
                                                  
                                                  <td>+$30,000</td>                                         
                                                </tr>
                                            </tbody>
            </table>
          </div>
            
        </div>
    </div>
</template>
<style scoped>
.icon{
  color: #0272A2;
  margin-right: 0.5rem;
  font-size: 20px;
}
.icono{
  font-size: 25px;
  color: grey;
}
.j{
  background: rgb(2, 216, 2);
  color: white;
  padding-top: 0.8rem;
  padding-left: 1.3rem;
  border-radius: 50%;
  height: 3rem;
  width: 3rem;
  margin-right: 0.5rem;
  display: inline-block;
}
.search{
  margin-left: 5%;
  margin-right: 5%;
  margin-top: 1rem;
  margin-bottom: 2rem;
}
.search input{
  width: 70%;
  border: 2px solid #dee2e6;
  background: url("/img/new/search.svg") no-repeat ;
  background-size: 1.3rem;
  background-position-x: 1rem;
  background-position-y: 6px;
  padding-left: 3rem;
  color: black;
  padding-top: 5px;
  padding-bottom: 5px;
}
.sb{
  width: 10%;
  border: 2px solid #dee2e6;
  margin-left: 5px;
  padding-top: 5px;
  padding-bottom: 5px;
}
.mo{
  width: 10%;
  border: 2px solid #dee2e6;
  margin-left: 7.2rem;
  padding-top: 5px;
  padding-bottom: 5px;
}
    .nav1{
        margin-top: 1rem;
      border-bottom: 1px solid #dee2e6;
    }
    nav{
      
      margin-left: 5%;
      margin-right: 5%;
    }
    .nav3{
      
      display: inline;
    }
   
    .nav-item{
        margin-left: 3rem;
    }
    .active{
        border-bottom: none;
    }
    a{
        color: black;
        
    }
    .small{
      display: none;
    }
    .ba{
         margin-left: 5%;
        margin-right: 5%;
        margin-top: 1rem;
        display: grid;
        grid-template-columns: 2fr 1fr 1fr;
    }
    .ba1{
      border-right: 2px solid #dee2e6;
    }
    .ba2{
      border-right: 2px solid #dee2e6;
      padding-left: 1rem;
    }
    .ba2 p{
      color: #0272A2;
    }
    .ba h1{
        color: #0272A2;
    }
    .ta{
        margin-left: 5%;
        margin-right: 5%;
        margin-top: 1rem;
    }
    th{
        background-color: #0272A2;
        color: white;
        
        border: none;
    }
    tr{
        background: white;
        margin-top: 5px;
        color: #0272A2;
    }
    table {
  border-collapse:separate; 
  border-spacing: 0 0.1em;
}


    @media(max-width:567px){
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
    .nav-tabs .nav-link.active, .nav-tabs .nav-item.show .nav-link {
    color: #495057;
    background-color: #fff;
    border-color: none;
}
.nav-tabs .nav-link {
    border: none  !important;
    border-top-left-radius: 0.25rem;
    border-top-right-radius: 0.25rem;
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