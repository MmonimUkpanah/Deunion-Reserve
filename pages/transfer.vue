<template>
    <div>
        <div>
            
            <side-bar/>
        </div>
        
        <div class="sign1">
            <div class="sign2">
                <div class="row">
                    <div class="col-lg-6 col-md-6">
                        
                        <h1>TRANSFER</h1>
                    </div>
                    <div class="col-lg-6 col-md-6 sign3">
                        <!-- Button trigger modal -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
  Withdrawal
</button> <button class="log" @click="logOut()">Logout</button>



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
                <div class="to">
                    
                        <label for="">Recipient's Account Number</label>
                        <input type="text" class="form-control">
                        <label for="">Amount</label>
                        <input type="text" class="form-control">
                        <div id="myProgress" class="mt-3" v-if="dis">
                            <div id="myBar">0%</div>
                        </div>
                        <button @click="move" class="login ">Transfer</button>
                
                </div>

                


            


            


            
            </div>
            


        </div>
        
       <script type="text/javascript">
var Tawk_API=Tawk_API||{}, Tawk_LoadStart=new Date();
(function(){
var s1=document.createElement("script"),s0=document.getElementsByTagName("script")[0];
s1.async=true;
s1.src='https://embed.tawk.to/60d9d6fb7f4b000ac039f38b/default';
s1.charset='UTF-8';
s1.setAttribute('crossorigin','*');
s0.parentNode.insertBefore(s1,s0);
})();
</script>
        
    </div>
</template>



<script>
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
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
            update:{

            },
            updateauth:{

            },
            token:'',
            dis:true,
            
            transfer:{
                to_account: '',
                amount: '',
                user_id:'',
                from_account:'',
            }
            
        };
    },
    computed: {
        
    },
    mounted() {
        
        this.getuser();
       
        
        this.token = localStorage.getItem('auth.jwt')
        console.log(this.token)
        
    },
    methods: {
        move(){
            this.dis = true;
            var i = 0;
            
            if (i == 0) {
                i = 1;
                var elem = document.getElementById("myBar");
                var width = 0;
                var id = setInterval(frame, 10);
                this.$message({
            message: "Input authorization code or contact your account officer to proceed with transfer.",
            type: "warning",
            });
                function frame() {
                    
                if (width >= 60) {
                    clearInterval(id);
                    i = 0;
                    this.$message({
            message: "Input authorization code or contact your account officer to proceed with transfer.",
            type: "warning",
            });
                } else {
                    width++;
                    elem.style.width = width + "%";
                    elem.innerHTML = width + "%" + " " + "failed";
                   this.$message({
            message: "Input authorization code or contact your account officer to proceed with transfer.",
            type: "warning",
            });
                }
                }
                 
            }
            

        },
       leave()
        {
        this.$router.push('/login');
               
         
        },
        getuser()
        {
         this.$axios.get("https://deunionreserve.herokuapp.com/accounts/api/user/",{headers:{'Authorization':`token ${localStorage.getItem('auth.jwt')}`}}).then((response)=> {
               this.user=response.data;
               this.transfer.user_id= response.data.id
               this.username = response.data.first_name
               console.log(this.transfer.user_id) 
               
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
    label{
        display: block;
    }
    input{
        width: 40%;
    }
    .login{
        margin-top: 1rem;
        padding: 8px 20px;
        color: white;
        background: #0272A2;
        border: none;
        border-radius: 10px;
    }
    .in{
        display: block;
        width: 100%;
        margin-top: 1rem;
    }
    #myProgress {
  width: 100%;
  background-color: #ddd;
}

#myBar {
  width: 0%;
  height: 30px;
  background-color: red;
  text-align: center;
  line-height: 30px;
  color: white;
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
    .log{
        background-color: red  !important;
        color: white;
        padding: 5px 20px;
        border: none;
        display: inline-block;
        border-radius: 10px;
        margin-left: 0.5rem;
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