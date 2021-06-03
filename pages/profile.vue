<template>
    <div class="login-1">
       <nav class="navbar navbar-expand-lg navbar-light small fixed-top">
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
        <div class="">
            <div class="login-3">
                
                <div style="">
                    
                    <ValidationObserver v-slot="{ invalid }">
                        <form @submit.prevent="updateProfile">
                        
                        <div class="login-2">
                            <h2>UPDATE PROFILE</h2>
                        <div class="grid">
                        <div class="form-group">
                            <label >FIRST NAME</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="name"
                                rules="required">
                            <input type="text" class="form-control" name="name" 
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
                                name="name"
                                rules="required">
                            <input type="text" class="form-control" name="name" 
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
                                name="name"
                                rules="required">
                            <input type="text" class="form-control" name="name" 
                            v-model="signup.surname" required>
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
                            <label >DATE OF BIRTH</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="dob"
                                rules="required">
                            <input type="date" class="form-control" name="dob" 
                            v-model="signup.dob" required>
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <label >PHONE</label>
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
                            <label >ACCOUNT TYPE</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="name"
                                rules="required">
                            <div class="input-group">
                                <select v-model="signup.account_type" class="form-select form-control" id="inputGroupSelect04" aria-label="Example select with button addon">
                                    <option  selected>Choose...</option>
                                    <option value="Savings">Savings</option>
                                    <option value="Current">Current</option>
                                
                                </select>
                                
                            </div>
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <label >NEXT OF KIN</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="name"
                                rules="required">
                            <input type="text" class="form-control" name="name" 
                            v-model="signup.next_of_kin" required>
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <label >RELATIONSHIP WITH NEXT OF KIN</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="name"
                                rules="required">
                            <input type="text" class="form-control" name="name" 
                            v-model="signup.relationship_nok" required>
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <label >PHONE NUMBER OF NEXT OF KIN</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="name"
                                rules="required">
                            <input type="text" class="form-control" name="name" 
                            v-model="signup.phone_nok" required>
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <label >ID FRONT VIEW</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="name"
                                rules="required">
                            <input
                                            required
                                                    type="file"
                                                    class="file-border img-fluid"
                                                    @change="uploadf()"
                                                    />
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <label >ID BACK VIEW</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="name"
                                rules="required">
                            <input
                                required type="file" class="file-border img-fluid" @change="uploadb()" />
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <label >PASSPORT</label>
                            <ValidationProvider
                                v-slot="{ errors }"
                                name="name"
                                rules="required">
                            <input
                                required type="file" class="file-border img-fluid" @change="uploadp()" />
                            <span class="input-invalid-message">
                                {{ errors[0] }}
                            </span>
                            </ValidationProvider>
                        </div>
                        <div class="form-group">
                            <button type="submit" :disabled="invalid" class="login">SUBMIT</button>
                        </div>
                        
                        
                        
                        
                        </div>
                        
                       <!-- <div>
                           <p>By clicking Create Account, you agree to ForexHup's<a href="/terms"> Terms and Conditions</a></p>
                       </div> -->
                       
                        
                
                        </div>
                        
                    </form>
                    </ValidationObserver>
                    
                    
                </div>
            </div>
        </div>
    </div>
</template>



<script>
import { ValidationObserver, ValidationProvider } from "vee-validate";
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';
import { mapGetters } from 'vuex'
export default {
    auth: false,
    components: {
    ValidationObserver: ValidationObserver,
    ValidationProvider: ValidationProvider
  },
    data(){
        return{
            signup: {
                passport:'',
                first_name: '',
                middle_name: '',
                surname: '',
                sex: '',
                dob: '',
                phone: '',
                email: '',
                valid_ID_frontview: '',
                valid_ID_backview: '',
                account_type: '',
                next_of_kin: '',
                relationship_nok:'',
                phone_nok: '',
                user_id:''
            },
            user:{

            },
            users:{

            },
            use:{

            }
            
        }
    },
    created(){
         
        this.use = this.$store.state.auth.loggedIn;
        console.log(this.use)
        this.getuser()
        
    },
    methods: {
        uploadf() {
      var input = event.target;
      this.signup.valid_ID_frontview = input.files[0];
      console.log(this.signup.valid_ID_frontview);
    },
    computed: {
    ...mapGetters(['isAuthenticated', 'loggedInUser'])
  },
    uploadb() {
      var input = event.target;
      this.signup.valid_ID_backview = input.files[0];
      console.log(this.signup.valid_ID_backview);
    },
    uploadp() {
      var input = event.target;
      this.signup.passport = input.files[0];
      console.log(this.signup.passport);
    },
        updateProfile(){
            const formData = new FormData();
            formData.append("passport", this.signup.passport);
            formData.append("first_name", this.signup.first_name);
            formData.append("middle_name", this.signup.middle_name);
            formData.append("surname", this.signup.surname);
            formData.append("sex", this.signup.sex);
            formData.append("dob", this.signup.dob);
            formData.append("phone", this.signup.phone);
            formData.append("email", this.signup.email);
            formData.append("valid_ID_frontview", this.signup.valid_ID_frontview);
            formData.append("valid_ID_backview", this.signup.valid_ID_backview);
            formData.append("account_type", this.signup.account_type);
            formData.append("next_of_kin", this.signup.next_of_kin);
            formData.append("relationship_nok", this.signup.relationship_nok);
            formData.append("phone_nok", this.signup.phone_nok);
            formData.append("user_id", this.signup.user_id);
            formData.append("_method", "POST");
            this.$axios
        .post("https://deunionreserve.herokuapp.com/accounts/api/updateuser/", formData)
        .then((res) => {
          this.$message({
            message:
              "Profile Updated",
            type: "success",
          });
          this.signup = {};
          this.$router.push("/userdashboard");
          console.log(res.data);
        }).catch((error) => {
          console.log(error);
        });
        

        },
        getuser()
        {
            this.$router.app.refresh()
         this.$axios.get("https://deunionreserve.herokuapp.com/accounts/api/user/",{headers:{'Authorization':`token ${localStorage.getItem('auth.jwt')}`}}).then((response)=> {
               this.user=response.data;
               this.signup.user_id= response.data.id
               console.log(this.signup.user_id) 
               
         }) 
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
    .icons{
      text-decoration: underline;
      font-weight: bold;
    }
    .grid4{
      display: grid;
      grid-template-columns: 1fr 1fr;
    }
    .grid1{
      text-align: right;
      margin-top: 7px;
    }

     .grid{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-column-gap: 1rem;
        color: white;
    }
    .login-1{
        background: white;
        
    }
    form{
        color: white !important;
        border-radius: 24px;
        margin-left: 5%;
        margin-right: 5%;
        display: block;
    }
    .login-2{
        padding: 2rem 4rem;
        
    }
    
    form h2{
        color: white;
        font-size: 40px;
        font-weight: bold;
        margin-bottom: 1rem;
    }
    a{
        text-decoration: none;
        color: #0272A2;
    }
    .form-group input,select{
        background: #F9F9FA  !important;
        border-radius: 8px;
        padding: 8px 8px;
        margin-bottom: 1rem;
        width: 100%;
    }
    form label{
        color: white;
        font-weight: bold;
    }
    .login{
        width: 100%;
        border: none;
        border-radius: 8px;
        margin-top: 2rem;
        padding: 11px;
        color: white !important;
        background-color: #0272A2;
    
    }
    .login-3{
        background: linear-gradient(
            to right,
            rgba(0, 4, 23, 0.58),
            rgba(0, 4, 23, 0.58)
        ),url(/img/new/ch.jpg) center center/cover;
        height: 100vh;
        
        
    }
    .login-3 h2{
        font-size: 45px;
        color:white;

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
        .login-2{
        padding: 2rem 10px;
        
    }
        form h2{
        color: #334D6E;
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
        background-color: white !important;
        border-radius: 10px;
        margin-left: 0;
        margin-right: 0;
        margin-top: 2rem;
        display: block;
    }
    form label{
        color: #334D6E;
        font-weight: bold;
    }
    .login-3{
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
    
    .login-3 h2{
        font-size: 45px;
        color: #334D6E;

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
        grid-template-columns: 1fr;
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