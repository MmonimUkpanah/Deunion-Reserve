<template>
    <div>
      <div class="show big">
      <ul>
        <li><h1>Deunion Reserve</h1></li> <li>Media</li> <span class="space">|</span>  <li>Careers</li> <span class="space">|</span>  <li>Research</li>
        <span class="space">|</span>  <li>Responsibility</li>
      </ul>
    </div>
        <nav class="navbar navbar-expand-lg navbar-light small fixed-top">
        <div class="container-fluid">
          <a class="navbar-brand" href="/" > <svg id="svgsymbol-logo"  viewBox="0 0 32 32"><path d="M4.5 4.5v23h23v-23h-23zM0 0h32v32H0V0zm7 24.3L19.2 7.7H25L12.8 24.3H7z"></path></svg> Deunion Reserve </a>
          
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo02" aria-controls="navbarTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item ic">
                <font-awesome-icon :icon="['fas', 'share-alt']" class="icon" /> <font-awesome-icon :icon="['fas', 'link']" class="icon" /> <nuxt-link to="contact"><font-awesome-icon :icon="['fas', 'envelope']" class="icon" /></nuxt-link> 
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
            <form action="" @submit.prevent="sendQuery()">
              <label for="">Name</label>
              <input type="text" class="form-control" required v-model="contact.name">
              <label for="">Email</label>
              <input type="email" name="" id="" class="form-control" required v-model="contact.email">
              <label for="">Phone Number</label>
              <input type="text" class="form-control" required v-model="contact.phone_number">
              <label for="">Query</label>
              <textarea name="" id="" class="form-control" v-model="contact.query"></textarea>
              <button class="login">Send</button>
            </form>
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
        <footer-sections/>
    </div>
</template>
<script>

import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css'
export default {
    
    data(){
        return{
          contact:{
            name:'',
            query:'', 
            email:'',
            phone_number:''
          } 
            
        }
    },
    created(){
         
      
        
    },
    methods: {
        
        sendQuery(){
            
            this.$axios
        .post("https://deunionreserve.herokuapp.com/customers/api/contactlist/", this.contact)
        .then((res) => {
          this.$message({
            message:
              "Query Sent",
            type: "success",
          });
          this.contact = {}
          console.log(res.data);
        }).catch((error) => {
          console.log(error);
        });
        

        },
        
        

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
    .show{
      padding-left: 2%;
      padding-right: 5%;
      margin-bottom: 3rem;
      margin-top: 1rem;
    }
    .show ul li{
      display: inline;
      font-size: 20px;
      
    }
    .show h1{
      margin-right: 1.5rem;
      color: #0272A2;
      display: inline;
    }
    .space{
        margin-left: 10px;
        margin-right: 10px;
        
        
    }
    .login{
      
        margin-top: 1rem;
        padding: 8px 20px;
        color: white;
        background: #0272A2;
        border: none;
        border-radius: 10px;
    }
    .show{
      padding-left: 3%;
      padding-right: 5%;
      margin-bottom: 3rem;
      margin-top: 1rem;
    }
    .show ul li{
      display: inline;
      font-size: 20px;
      
    }
    .show h1{
      margin-right: 1.5rem;
      color: #0272A2;
      display: inline;
    }
    input{
      width: 30%;
      margin-bottom: 1rem;
    }
    textarea{
      width: 30%;
      height: 7rem;
    }
    label{
      display: block;
    }
    .con{
        margin-left: 5%;
        margin-right: 5%;
        margin-top: 3rem;
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

    .nav-item{
        margin-left: 3rem;
    }
    .active{
        border-bottom: 1px solid #dee2e6  !important ;
    }
    a{
        color: black;
    }
    .navbar-brand{
      color: #0272A2;
    }
    .navbar-brand svg{
      background-color: #0272A2  !important;
      width:1.7rem ;
      margin-right: 0.3rem;
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
    .login{
      width: 100%;
        margin-top: 1rem;
        padding: 8px 20px;
        color: white;
        background: #0272A2;
        border: none;
        border-radius: 10px;
    }
    input{
      width: 100%;
      margin-bottom: 1rem;
    }
    textarea{
      width: 100%;
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
        margin-top: 4rem;
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
    }
</style>