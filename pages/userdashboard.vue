<template>
    <div>
        <div>
            
            <side-bar/>
        </div>
        
        <div class="sign1">
            <div class="sign2">
                <div class="row">
                    <div class="col-lg-6 col-md-6">
                        
                        <h1>Welcome <span style="text-transform:capitalize">{{this.username}}</span>.</h1>
                    </div>
                    <div class="col-lg-6 col-md-6 sign3">
                        <!-- Button trigger modal -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
  Withdrawal
</button>

<!-- Modal -->
<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">WITHDRAWAL</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        Please contact your account officer for authorization code to proceed with withdrawal
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Proceed</button>
        
      </div>
    </div>
  </div>
</div>
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
            user:{},
            account:{},
            username:''
            
        };
    },
    computed: {
        
    },
    methods: {
        getuser()
        {
         this.$axios.get("https://deunionreserve.herokuapp.com/accounts/api/user/",{headers:{'Authorization':`token ${localStorage.getItem('auth.jwt')}`}}).then((response)=> {
               this.user=response.data;
               this.username = response.data.username
               console.log(this.user) 
               
         }) 
        },
        getaccount()
        {
         this.$axios.get("https://deunionreserve.herokuapp.com/customers/api/customersaccountlist/",{headers:{'Authorization':`token ${localStorage.getItem('auth.jwt')}`}}).then((response)=> {
               this.account=response.data;
               console.log(this.account) 
               
         }) 
        }
        
    },
    mounted() {
        
        this.getuser();
        this.getaccount()
        
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
        padding-top: 2rem;
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