<template>
    <div>
        <div>
            <nav class="navbar navbar-expand-lg navbar-light small">
        <div class="container-fluid">
          <a class="navbar-brand" href="/">Deunion Reserve</a>
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
              <!-- <li class="nav-item">
                <a class="nav-link" href="/login">Client Login</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="/signup">Client Registration</a>
              </li> -->
              
            </ul>
            
          </div>
        </div>
      </nav>
            <side-bar/>
        </div>
        
        <div class="sign1">
            <div class="sign2">
                <div class="row">
                    <div class="col-lg-6 col-md-6">
                        
                        <h1>Welcome <span style="text-transform:capitalize"></span>.</h1>
                    </div>
                    <div class="col-lg-6 col-md-6 sign3">
                        <button class="sign4">Fund Account</button><button>Invest Now</button>
                    </div>
                </div>
                <div class="car">
                    <h1>Account Information</h1>
                    <p>Account Name:</p>
                    <p>Account Number:</p>
                    <p>Available Balance:</p>
                    <p>Account Status:</p>

                </div>

                


            


            


            
            </div>
            


        </div>
        
       
        
    </div>
</template>



<script>

export default {
    auth: false,
    // layout: "blog",
    components: {
        
    },
    data() {
        return {
            signals:[],
            user:{},
            plan: '',
            signal: '',
            silversignals: {},
            goldsignals: {},
            displayGold: false,
            displaySilver: false,
            displayFree: true,
        };
    },
    computed: {
        
    },
    methods: {
        getSignals() {
            this.$axios
                .get("https://api.fxhup.com/project/signals")
                .then((res) => {
                    console.log(res.data.data);
                    this.signals = res.data.data.signals;
                    console.log(this.signals);
                    

                
                });
        },
        getSilver() {
            this.$axios
                .get("https://api.fxhup.com/project/silver")
                .then((res) => {
                    console.log(res.data.data);
                    this.silversignals = res.data.data.silver;
                    console.log(this.silversignals);
                    

                
                });
        },
        getGold() {
            this.$axios
                .get("https://api.fxhup.com/project/gold")
                .then((res) => {
                    console.log(res.data.data);
                    this.goldsignals = res.data.data.gold;
                    console.log(this.goldsignals);
                    

                
                });
        },
        getUser() {
            this.$axios
                .get("https://api.fxhup.com/auth/user")
                .then((res) => {
                    console.log(res.data);
                    this.user = res.data.data;
                    console.log(this.user);
                    this.plan = res.data.data.user_plan.display_name;
                    console.log(this.plan);
                    if (this.plan == 'Silver'){
                        this.displaySilver = true;
                        this.displayFree = false;
                    }else{this.displaySilver = false};
                    if (this.plan == 'Gold'){
                        this.displayGold = true;
                        this.displayFree = false;
                    }else {
                        this.displayGold = false
                    }
                    
                    
                });
        },
        
    },
    mounted() {
        this.getSignals();
        this.getUser();
        this.getGold();
        this.getSilver();
    },
};
</script>
<style scoped>
     @font-face {
    font-family: DMSans;
    src: url("/font/DMSans-Regular.ttf");
    }
    *{
        font-family: 'DM Sans', sans-serif  !important;
        box-sizing: border-box;
    }
    .link:hover{
        text-decoration: none;
    }
    .upgrade{
        background: #DE911D;
        padding: 1rem 1rem;
        margin-top: 1rem;
        border-radius: 10px;
        color: white;
    }
    .grid{
        display: grid;
        grid-template-columns: 2fr 1fr;
        grid-column-gap: 1rem;
    }
    .grade{
        text-align: right;
    
    }
    .grade button{
        background: #F0B429;
        margin-top: 2.5rem;
        padding: 8px 2rem;
        border-radius: 8px;
        border: none;
        color:white;
    }
    .sign1{
        margin-left: 20%;
        background: #F4FAFD;
        height: 120vh;
        padding-top: 2rem;
        
        
    }
    .sign2{
        margin-left: 4rem;
        margin-right: 4rem;
    }
    .sign2 h1{
        font-size: 40px;
        color: #0272A2;
        font-weight: bold;
    }
    .sign3{
        margin-top: 10px;
    }
    .sign3 button{
        background-color: #0272A2;
        color: white;
        padding: 5px 20px;
        border: none;
        border-radius: 10px;
    }
    .sign4{
        margin-right: 10px;
    }
    .sign3 img{
        border-radius: 50%;
        width: 50px;
        height: 50px;
        margin-top: 4rem;
    }
    th{
        background-color: #0272A2;
        color: white;
        
        border: none;
    }
    .borderleft{
        border-bottom-left-radius: 10px  !important;
        border-top-left-radius: 10px  !important;
    }
    .borderright{
        border-bottom-right-radius: 10px  !important;
        border-top-right-radius: 10px  !important;
    }
    tr{
        background: white;
        margin-top: 5px;
        color: #0272A2;
    }
    table {
  border-collapse:separate; 
  border-spacing: 0 0.5em;
}
.nav-item{
        margin-left: 6rem;
    }
    a{
        color: black !important;
    }
    .car{
        margin-top: 2rem;
        
    }

@media(max-width:576px){
    .upgrade{
        background: #DE911D;
        padding: 2rem 1rem;
        margin-top: 1rem;
        border-radius: 10px;
        color: white;
    }
    .grid{
        display: grid;
        grid-template-columns:1fr;
        grid-column-gap: 1rem;
    }
    .grade{
        text-align: center;
    
    }
    .grade button{
        background: #F0B429;
        margin-top: 2.5rem;
        padding: 8px 2rem;
        border-radius: 8px;
        border: none;
        color:white;
    }
       .sign1{
        margin-left: 0%;
        background: #F4FAFD;
        height: 120vh;
        padding-top: 2rem;
        
    }
    .sign2{
        margin-left: 1rem;
        margin-right: 1rem;
    }
    .nav-item{
        margin-left: 0rem;
    }
}

@media (min-width:577px) and (max-width:768px){
    .sign1{
        margin-left: 0%;
        background: #F4FAFD;
        height: 100vh;
        padding-top: 3rem;
        
    }
}
@media (min-width:769px) and (max-width: 1200px){
    .sign1{
        margin-left: 25%;
        background: #F4FAFD;
        height: 120vh;
        padding-top: 2rem;
        
        
    }
}

</style>