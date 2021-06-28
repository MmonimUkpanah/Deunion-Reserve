<template>
    <div class="login-1">
       <nav class="navbar navbar-expand-lg navbar-light small fixed-top">
        <div class="container-fluid">
          <a class="navbar-brand" href="/" > <svg id="svgsymbol-logo"  viewBox="0 0 32 32"><path d="M4.5 4.5v23h23v-23h-23zM0 0h32v32H0V0zm7 24.3L19.2 7.7H25L12.8 24.3H7z"></path></svg> Deunion Reserve </a>
          
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo02" aria-controls="navbarTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item ic">
                <font-awesome-icon :icon="['fas', 'share-alt']" class="icon" /> <font-awesome-icon :icon="['fas', 'link']" class="icon" /> <font-awesome-icon :icon="['fas', 'envelope']" class="icon" />
              </li>
              <li class="nav-item grid4">
                <a class="nav-link icons" href="/">Deunion Reserve </a><span class="grid1"><font-awesome-icon :icon="['fas', 'home']" class="" /></span>
              </li>
              <li class="nav-item grid4">
                <a class="nav-link active" aria-current="page" href="/do">What we do </a><span class="grid1"><font-awesome-icon :icon="['fas', 'chevron-circle-right']" class="ico" /></span>
              </li>
              <li class="nav-item grid4">
                <a class="nav-link" href="/we">Who we are </a><span class="grid1"><font-awesome-icon :icon="['fas', 'chevron-circle-right']"  /></span>
              </li>
              <li class="nav-item grid4">
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
                    <a class="nav-link"  href="/do">What we do</a>
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
                    <a class="nav-link  active" aria-current="page" href="/signup">Client Registration</a>
                </li>
            </ul>
        </div>
        <div class="container-fluid">
            <div class="row">
                <div class="col-md-6 login-3">
                    
                </div>
                <div class="col-md-6">
                   
                    <ValidationObserver v-slot="{ invalid }">
                        <form method="post"  @submit.prevent="signUp">
                        
                        <div class="login-2">
                            <h2>REGISTRATION</h2>
                        <div class="grid">
                            <div class="form-group">
                            <label >FIRST NAME</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="first_name"
                                rules="required">
                            <input type="text" class="form-control" name="first_name" 
                            v-model="signup.first_name" required>
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                            </div>
                        <div class="form-group">
                            <label >MIDDLE NAME</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="middle_name"
                                rules="required">
                            <input type="text" class="form-control" name="middle_name" 
                            v-model="signup.middle_name" required>
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <label >SURNAME</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="surname"
                                rules="required">
                            <input type="text" class="form-control" name="surname" 
                            v-model="signup.surname" required>
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <label>EMAIL</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="email"
                                rules="required|email">
                            <input type="email" class="form-control" @keydown.space.prevent 
                            v-model="signup.email" required>
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <label >PHONE NUMBER</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="phone"
                                rules="required">
                            <input type="text" class="form-control" name="phone" 
                            v-model="signup.phone" required>
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                         <div class="form-group">
                            <label >SEX</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="name"
                                rules="required">
                            <div class="input-group">
                                <select v-model="signup.sex" class="form-select form-control" id="inputGroupSelect04" aria-label="Example select with button addon">
                                    <option  selected>Choose...</option>
                                    <option value="M">Male</option>
                                    <option value="F">Female</option>
                                
                                </select>
                                
                            </div>
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>          
                        <div class="form-group">
                            <label>PASSWORD</label>
                            <ValidationProvider rules="min:8|required" v-slot="{ errors }" vid="signup.password" name="password">
                            <input type="password" class="form-control" @keydown.space.prevent v-model="signup.password">
                            <span class="input-invalid-message">{{ errors[0] }}</span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <label> CONFIRM PASSWORD</label>
                            <ValidationProvider rules="confirmed:signup.password|min:8|required" name="Confirm Password" v-slot="{ errors }">
                            <input type="password" class="form-control" @keydown.space.prevent v-model="signup.password2">
                            <span class="input-invalid-message">{{ errors[0] }}</span>
                            </ValidationProvider>
                        </div>
                        </div>
                        
                       <!-- <div>
                           <p>By clicking Create Account, you agree to ForexHup's<a href="/terms"> Terms and Conditions</a></p>
                       </div> -->
                       
                        <button type="submit" :disabled="invalid" class="login">SUBMIT</button>
                
                        </div>
                        
                    </form>
                    </ValidationObserver>
                    
                    
                </div>
            </div>
        </div>
        <script type="text/javascript">
var Tawk_API=Tawk_API||{}, Tawk_LoadStart=new Date();
(function(){
var s1=document.createElement("script"),s0=document.getElementsByTagName("script")[0];
s1.async=true;
s1.src='https://embed.tawk.to/607873c3067c2605c0c2cc88/default';
s1.charset='UTF-8';
s1.setAttribute('crossorigin','*');
s0.parentNode.insertBefore(s1,s0);
})();
</script>
    </div>
</template>



<script>
import { ValidationObserver, ValidationProvider } from "vee-validate";
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
export default {
    auth: false,
    components: {
    ValidationObserver: ValidationObserver,
    ValidationProvider: ValidationProvider
  },
    data(){
        return{
            signup: {
                first_name:'',
                middle_name:'',
                surname:'',
                sex:'',
                phone: '',
                email: '',
                password: '',
                password2: ''
            }
            
        }
    },
    mounted(){
    
    },
    methods: {
    async signUp() {
      try {
        let response = await this.$axios.post("https://deunionreserve.herokuapp.com/accounts/api/register/",this.signup);
        let user = response.data.user;
            this.$auth.$storage.setLocalStorage("user", user);
            let token = response.data.token;
            this.$auth.$storage.setLocalStorage("jwt", token);
        
        console.log(response)
        this.$message({
            message: "Account created successfully!",
            type: "success",
            });
            this.$router.push("/profile");
      } catch (err) {
        console.log(err)
        this.$message({
            message: "There was a problem creating your account. Please try again.",
            type: "warning",
            });
      }
    }
    //  signUp()
    //     {
            
    //          this.$axios.post("https://deunionreserve.herokuapp.com/accounts/api/register/",this.signup)
    //         .then((res)=> {
    //          console.log(res)
    //           this.$message({
    //          message: "Account created successfully!",
    //         type: "success",
    //        });
    //        this.$auth.loginWith('local', { data: this.signup })
           
    //        this.$router.push("/profile");
          
    //         })
    //         .catch((error)=> {
    //         console.log(error)
    //         this.$message({
    //          message: "There was a problem creating your account. Please try again.",
    //         type: "warning",
    //         });
            
            
    //         })
            
         
    //     },
  }
    
}

</script>




<style scoped>
@font-face {
    font-family: DMSans;
    src: url("/font/DMSans-Regular.ttf");
    }
    *{
        font-family: 'DM Sans', sans-serif  !important;
        
    }
    .input-invalid-message{
        color: red;
    }
    .icons{
      text-decoration: underline;
      font-weight: bold;
    }
    .grid4{
      display: grid !important;
      grid-template-columns: 2fr 1fr;
    }
    .grid1{
      text-align: right;
      margin-top: 7px;
    }

    .login-1{
        background: white;
        
    }
    form{
        background-color: #FFFFFF !important;
        border-radius: 24px;
        margin-top: 0rem;
    }
    .login-2{
        padding:2rem 4rem ;
        
    }
    
    form h2{
        color: #0272A2;
        font-size: 40px;
        font-weight: bold;
        margin-bottom: 1rem;
    }
    a{
        text-decoration: none;
        color: #0272A2;
    }
    .form-group input{
        background: #F9F9FA  !important;
        border-radius: 8px;
        padding: 8px 8px;
        margin-bottom: 1rem;
        width: 100%;
    }
    form label{
        color: #0272A2;
        font-weight: bold;
    }
    .navbar-brand{
      color: #0272A2;
    }
    .navbar-brand svg{
      background-color: #0272A2  !important;
      width:1.7rem ;
      margin-right: 0.3rem;
    }
    .login{
        width: 100%;
        padding: 8px 0;
        border: none;
        border-radius: 8px;
        color: white !important;
        background-color: #0272A2;
        margin-top: 1rem;
    }
    .login-3{
        background: linear-gradient(
            to right,
            rgba(0, 4, 23, 0.58),
            rgba(0, 4, 23, 0.58)
        ),url(/img/new/ch.jpg) center center/cover;
        height: 92.3vh;
        margin-top: -1px;
        
    }
    .login-3 h2{
        font-size: 45px;
        color: #01445F;

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
    .nav1{
        margin-top: 1rem;
    
    }
    .grid{
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-column-gap: 1rem;
    }


    @media(max-width: 576px){
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
        form h2{
        color: white;
        font-size: 35px;
        font-weight: bold;
        margin-bottom: 2rem;
    }
        .login-1{
        padding-top: 10px;
        background: #F4FAFD;
        height: auto;
    }
    form{
        background-color: #FFFFFF !important;
        border-radius: 10px;
        margin-top: 2rem;
    }
    form label{
        color: white;
        font-weight: bold;
    }
    .login-2{
        padding:3rem 1rem ;
        background: linear-gradient(
            to right,
            rgba(0, 4, 23, 0.58),
            rgba(0, 4, 23, 0.58)
        ),url(/img/new/ch.jpg) center center/cover;
        height: auto;
        margin-top: 4rem;
    }
    .login{
        width: 100%;
    }
    .login-3{
        display: none;
        
    }
    .login-3 h2{
        font-size: 45px;
        color: white;

    }
    input{
        background: #F9F9FA;
        border-radius: 8px;
        padding: 8px 8px;
        margin-bottom: 1.5rem;
        width: 100%;
    }
    .grid{
        display: grid;
        grid-template-columns: 1fr ;
    }
    .small{
      display:block;
      background: white;
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
    .for{
        text-align: center;
        margin-top: 1rem;
        color: white;
    }
    .for a{
        color: white;
    }
    .form-group input{
        background: #F9F9FA  !important;
        border-radius: 8px;
        padding: 8px 8px;
        margin-bottom: 1rem;
        width: 100%;
    }
    }
</style>