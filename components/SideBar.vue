<template>
    <div class="one">
        <div class="one1">
            
            
       
        </div>
        <!-- <div class="grid1">
            
            
            <span class="two dropdown-item rout link" style="font-weight:bold; font-size:25px">Deunion Reserve</span>
        </div> -->
         <div class="grid1">
            <router-link to="/userdashboard" class="dropdown-item rout link" >
           
            <span class="two">Dashboard</span></router-link>
        </div>


        <div class="grid1">
            <router-link to="/transfer" class="dropdown-item rout link" >
           
            <span class="two">Transfer</span></router-link>
        </div>
         
        
        <div class="grid1" @click="logOut">
            <div class="dropdown-item rout link">
               
            <span class="two"> Log Out</span>
            </div>
            
        </div>
        <!-- <div class="grid1">
            <router-link to="/addstudent" class="dropdown-item link" >
            <font-awesome-icon class="icon" :icon="['fas', 'headset']" />
            <span class="two"> Support</span></router-link>
        </div> -->
        <div>
            
        </div>
            

        
        <!-- <div class="grid1">
            <router-link to="/viewstudents" class="dropdown-item" ><span class="two">View Students</span></router-link>
        </div> -->
    
        
        <!-- <hr>
        <div class="grid1">
            <router-link to="/addsession" class="dropdown-item" ><span class="two">Add Session</span></router-link>
        </div>
        <div class="grid1">
            <router-link to="/viewsessions" class="dropdown-item" ><span class="two">View Sessions</span></router-link>
        </div> -->
         
        
    </div>

</template>

<script>
export default {
   
    methods:{
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
  }
    
    
};
</script>

<style scoped>
*{
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.icon{
    width: 20px;

}
.icons{
    font-size: 15px;
    
    margin-left: 10px;
}

.one{
    width: 20%;
    height: 100vh;
    position: fixed;
    margin-top: 4rem;
    top: 0;
    left: 0;
    background: #FFFFFF;
    box-shadow: 6px 0px 18px rgba(0, 0, 0, 0.06);
    padding-top: 0rem;
    z-index: 1;
    

}
.two{
    font-size: 20px;
    color: #334D6E;
    padding: 7px 5px;
    font-weight:normal;
}





.one1{
    margin-left: 10px;
    margin-right: 10px;
    text-align: left;
    padding-top: 20px;
}
.one1 img{
    margin-bottom: 30px;
    padding-top: 20px;
}
.grid1{
    text-align: left;
    margin-left: 15px;
    margin-right: 10px;
    grid-gap: 0rem;
    margin-bottom: 30px;
    cursor: pointer;
    
}
.rout{
    padding: 10px 5px;
}

.grid1 img{
    margin-right: 20px;
}
.grid1 p{
    font-size: 20px;
    color: #334D6E;

}
.three{
    padding-left: 2rem;
}
.three p{
    font-size: 17px;
    color: #334D6E;
    
}
.iconz{
    font-size: 15px;
    margin-right: 5px;
    
}
hr{
    background: #EBEFF2 !important;
    margin-bottom: 30px;
    
}
p.hover{
    text-decoration: none;
}
.btn1{
    outline: none;
}
.dropdown{
    text-align: left !important;
}

@media(max-width: 576px){
    .one{
        display: none;
    }
}



@media (min-width: 577px) and (max-width: 768px){
    .one{
   display: none;
    

}
}
@media (min-width: 769px) and (max-width: 1200px){
    .one{
    width: 25%;
    height: 100vh;
    position: fixed;
    margin-top: 4rem;
    top: 0;
    left: 0;
    background: #FFFFFF;
    box-shadow: 6px 0px 18px rgba(0, 0, 0, 0.06);
    padding-top: 0rem;
    z-index: 1;
    

}
}
</style>