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
                    <a class="nav-link "  href="/contact">Contact Us</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="/login">Client Login</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/signup">Client Registration</a>
                </li>
            </ul>
        </div>
        <div class="container-fluid">
            <div class="row">
                <div class="col-md-6 login-3">
                    
                </div>
                <div class="col-md-6">
                    <ValidationObserver v-slot="{ invalid }">
                    <form method="post" @submit.prevent="userLogin">
                        
                        <div class="login-2">
                            <h2>LOGIN</h2>
                        <div class="form-group">
                            <label for="inputAddress2">EMAIL</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="email"
                                rules="required|email">
                            <input type="email" class="form-control" name="email"  
                             v-model="login.email">
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <label for="inputAddress2">PASSWORD</label>
                            <ValidationProvider rules="min:8|required" v-slot="{ errors }"  name="password">
                            <input type="password" class="form-control" name="password" v-model="login.password">
                            <span class="input-invalid-message">{{ errors[0] }}</span>
                            </ValidationProvider>
                        </div>
                
                        <button type="submit" :disabled="invalid" class="login">LOG IN</button>
                        <div class="for">
                            <p>Forgotten password? <a href="password"> Click here</a></p>
                        </div>
                        
                        </div>
                        
                    </form>
                    </ValidationObserver>
                </div>
            </div>
        </div>
    </div>
</template>



<script>
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
import { ValidationObserver, ValidationProvider } from "vee-validate";
export default {
    components: {
    ValidationObserver: ValidationObserver,
    ValidationProvider: ValidationProvider
  },
    data(){
        return{
            login: {
        email: '',
        password: ''
      }
            
        }
    },
    mounted(){
    
    },
    methods: {
    async userLogin() {
      try {
           let response = await this.$axios.post("https://deunionreserve.herokuapp.com/accounts/api/login/",this.login);
        // let response = await this.$auth.loginWith('local', { data: this.login })
            let user = response.data.user;
            this.$auth.$storage.setLocalStorage("user", user);
            let token = response.data.token;
            this.$auth.$storage.setLocalStorage("jwt", token);
            
            localStorage.setItem("jwt", token);
            
            console.log(user)
            console.log(token)
            console.log(response);
           
        
        this.$message({
              message: 'Welcome back',
              type: "success",
            });
        
             this.$router.push('/userdashboard');           
        console.log(response)
      } catch (err) {
           this.$message({
            message: "There was a problem logging into your account. Please try again.",
            type: "warning",
            });
        console.log(err)
      }
    }
  }
    // login(){
    //          this.$axios.post('https://api.fxhup.com/auth/contact', this.messageInfo,
    //           {headers : {'Content-Type':'application/json'}}).then((res)=> {
    //               this.$auth.loginWith('local')
    //             this.messageResponse=res.data;

    //            console.log(this.messageResponse);
    //            this.$message({
    //         message:"Message Sent!",
    //         type: "success",
    //       });this.messageInfo={};

    //         }).catch((error) => {
    //       console.log(error);
        
    //     });
           
    //     },
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
    .navbar-brand{
      color: #0272A2;
    }
    .input-invalid-message{
        color: red;
    }
    .navbar-brand svg{
      background-color: #0272A2  !important;
      width:1.7rem ;
      margin-right: 0.3rem;
    }
    .for{
        text-align: center;
        margin-top: 1rem;
    }
    .login-1{
        background: white;
    }
    form{
        background-color: #FFFFFF !important;
        border-radius: 24px;
        margin-top: 2rem;
    }
    .grid{
      display: grid !important;
      grid-template-columns: 2fr 1fr;
    }
    .icons{
      text-decoration: underline;
      font-weight: bold;
    }
    .grid1{
      text-align: right;
      margin-top: 7px;
    }

    .login-2{
        padding:1rem 4rem ;
    }
    form h2{
        color: #0272A2;
        font-size: 40px;
        font-weight: bold;
        margin-bottom: 2rem;
    }
    input{
        background: #F9F9FA;
        border-radius: 8px;
        padding: 8px 8px;
        margin-bottom: 1rem;
    }
    form label{
        color: #0272A2;
        font-weight: bold;
    }
    .login{
        width: 100%;
        margin-top: 1rem;
        padding: 8px 0;
        color: white;
        background: #0272A2;
        border: none;
        border-radius: 10px;
    }
    .login-3{
        background: linear-gradient(
            to right,
            rgba(0, 4, 23, 0.58),
            rgba(0, 4, 23, 0.58)
        ),url(/img/new/ch.jpg) center center/cover;
        height: 92.9vh;
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
        .login-1{
        padding-top: 10px;
        background: #F4FAFD;
        height: 100vh;
    }
    form label{
        color: white;
        font-weight: bold;
    }
    form h2{
        color: white;
        font-size: 40px;
        font-weight: bold;
        margin-bottom: 2rem;
    }
    form{
        background-color: #FFFFFF !important;
        border-radius: 10px;
        margin-top: 2rem;
    
    }
    .login-2{
        padding:3rem 1rem ;
        background: linear-gradient(
            to right,
            rgba(0, 4, 23, 0.58),
            rgba(0, 4, 23, 0.58)
        ),url(/img/new/ch.jpg) center center/cover;
        height: 100vh;
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
    }
    .small{
      display:block;
      background:white;
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
    }
</style>