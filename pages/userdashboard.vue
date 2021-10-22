<template>
    <div>
        <div class="di">
            <div class="di1">
                <h3>Deunion Reserve</h3>
            </div>
            <div class="di2">
                <img :src="this.user.passport" alt class="rounded-circle"/>
            </div>
        </div>
        <div>
            
            <side-bar/>
        </div>

        
        
        <div class="sign1">
            <div class="sign2">
                <div class="gi">
                    <div class="gi1">
                        <img src="/img/new/ru.jpg" alt="">
                    </div>
                    <div class="gi2">
                        <h3>Account Information</h3>
                        <p>Account Name: {{user.surname}}, {{user.middle_name}} {{user.first_name}}</p>
                        <p>Account Number: {{user.account_number}}</p>
                        <div class="sign3">
                        <!-- Button trigger modal -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
  Withdrawal
</button> <button class="log" @click="logOut()">Logout</button><nuxt-link to="transfer"><button type="button" class="btn btn-primary ko" >
  Transfer
</button></nuxt-link>



<!-- Modal -->
<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">WITHDRAWAL</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        
      </div>
      <div class="modal-body">
        Input authorization code or contact your account officer to proceed with withdrawal.
        <input type="text" class="form-control in" placeholder="Withdrawal code">
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Proceed</button>
        
      </div>
    </div>
  </div>
</div>
                    </div>
                    </div>
                    <div class="gi3">
                        <h3>Available Funds</h3>
                        <p>Balance: {{user.available_bal}}</p>
                    </div>
                </div>
               
                
                <div class="car">
                    <h1>Transaction History</h1>
                </div>
                <div class="ta">
          <div class="table-responsive">
            <table class="table  table-striped table-hover">
                                            <thead>
                                                <tr>
                                                <th scope="col">Transaction</th>
                                                <th scope="col">Details</th>
                                                <th scope="col">Amount</th>
                                                <th scope="col">Date</th>
                                                <th scope="col">Transaction ID</th>
                                                
                                                
                                                
                                                <th scope="col">Status</th>            
                                                </tr>
                                            </thead>
                                            <tbody>
                                                <tr v-for="(tran,id) in history" :key="id" > 
                                                  <td scope="row">{{tran.transaction_description}}</td>
                                                  <td>{{tran.transaction_type}}</td>
                                                  <td>{{tran.transaction_amount}}</td>
                                                  <td >{{tran.transaction_date}}</td>
                                                  <td >{{tran.transaction_id}}</td>
                                                  
                                                   
                                                  <td :class="[{'positive':tran.status = 'Successful'}]">{{tran.status}}</td>                                        
                                                </tr>
                                                
                                                
                                            </tbody>
            </table>
          </div>
            
        </div>


            


            


            
            </div>
            


        </div>
        
       
       <script type="text/javascript">
var Tawk_API=Tawk_API||{}, Tawk_LoadStart=new Date();
(function(){
var s1=document.createElement("script"),s0=document.getElementsByTagName("script")[0];
s1.async=true;
s1.src='https://embed.tawk.to/60dc40357f4b000ac03a4ec1/1f9e5llf2';
s1.charset='UTF-8';
s1.setAttribute('crossorigin','*');
s0.parentNode.insertBefore(s1,s0);
})();
</script>
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
            account:[],
            username:'',
            person:{

            },
            email:'',
            update:{

            },
            updateauth:{

            },
            token:'',
            history:{}
            
        };
    },
    computed: {
        
    },
    mounted() {
        
        this.getuser();
        this.gethistory();
        
        this.token = localStorage.getItem('auth.jwt')
        console.log(this.token)
        
    },
    
    methods: {
       leave()
        {
        this.$router.push('/login');
               
         
        },
        getuser()
        {
         this.$axios.get("https://deunion-reserve.herokuapp.com/accounts/api/user/",{headers:{'Authorization':`token ${localStorage.getItem('auth.jwt')}`}}).then((response)=> {
               this.user=response.data;
               this.username = response.data.first_name 
               this.email = response.data.email
               console.log(this.email)
               
         }) 
        },
        gethistory()
        {
         this.$axios.get('https://deunion-reserve.herokuapp.com/accounts/api/historylist/' ,{headers:{'Authorization':`token ${localStorage.getItem('auth.jwt')}`}}).then((response)=> {
               this.history=response.data;
               console.log(this.history) 
               
         }) 
        },
        
        
       
        async logOut() {
           
      
      try {
           
           
        this.$router.push('/login');
        this.$message({
              message: "You've logged out",
              type: "success",
            });
        
                        
        
      } catch (err) {
           this.$message({
            message: "There was a problem logging out. Please try again.",
            type: "warning",
            });
        console.log(err)
      }
    }
        
        
    },
    async fetch(){
        await this.gethistory()
    }
    
    
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
     .positive{
        background:green;
        color:white;
    }
    .negative{
        background: red;
        color:white;
    }
    .di{
        display: grid;
        grid-template-columns: 1fr 1fr;
        padding-top: 0.5rem;
        padding-bottom: 0.5rem;
        position: fixed;
        width: 100%;
        background-color: white;
    }
    .di1 h3{
        font-weight: bold;
        font-size: 35px;
        color: #334D6E;
        margin-left: 1.5rem;
    }
    .di2{
        text-align: right;
        margin-right: 1.5rem;
    }
    .gi{
        display: grid;
        grid-template-columns: 1.5fr 1fr 1fr;
        grid-column-gap: 2rem;
    }
    .gi h3{
        color: #0272A2;
    }
    .gi p{
        color: #334D6E;
    }
    .gi2{
        padding-top: 1rem;
    }
    .gi3{
        padding-top: 1rem;
    }
    .gi1 img{
        width: 100%;
    }
    .rounded-circle{
        height: 50px;
        width:50px;
        border: 2px solid #0272A2;
    }
    .in{
        display: block;
        width: 100%;
        margin-top: 1rem;
    }
    .ta{
        
        margin-top: 1rem;
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
    .ko{
        display: none;
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
        padding-top: 4rem;
        
        
    }
    .sign2{
        margin-left: 4rem;
        margin-right: 4rem;
        padding-top: 2rem;
    }
    .sign2 h1{
        font-size: 30px;
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
    .log{
        display: none;
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
    .gi{
        display: grid;
        grid-template-columns: 1fr ;
        grid-column-gap: 2rem;
    }
    .di{
        grid-template-columns: 1fr ;
        text-align: center;
    }
    .di1 h3{
        font-weight: bold;
        font-size: 30px;
        color: #334D6E;
        margin-left: 0rem;
    }
    .di2{
        display: none;
    }
    .log{
        background-color: red  !important;
        color: white;
        padding: 5px 20px;
        border: none;
        display: inline-block;
        border-radius: 10px;
        margin-left: 0.5rem;
    }
     .rounded-circle{
        height: 50px;
        width:50px;
        border: 2px solid #0272A2;
    }
    .ko{
        display: block;
        margin-top: 0.7rem;
    }
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
        height: auto;
        padding-top: 3rem;
        
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
      .rounded-circle{
        height: 50px;
        width:50px;
        margin-top: 0rem;
        margin-left: 10px;
        border: 2px solid #0272A2;
    }
    .gi{
        display: grid;
        grid-template-columns: 2fr 2fr 1fr;
        grid-column-gap: 2rem;
    }
    .sign2{
        margin-left: 1rem;
        margin-right: 1rem;
    }
    .gi2{
        padding-top: 0rem;
    }
    .gi3{
        padding-top: 0rem;
    }
}
@media (min-width:769px) and (max-width: 1200px){
    .sign1{
        margin-left: 20%;
        background: #F4FAFD;
        height: 120vh;
        padding-top:3rem;
    }
     .gi{
        display: grid;
        grid-template-columns: 2fr 2fr 1fr;
        grid-column-gap: 2rem;
    }
    .gi2{
        padding-top: 0rem;
    }
    .gi3{
        padding-top: 0rem;
    }
}

</style>