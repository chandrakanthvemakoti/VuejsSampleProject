<template>
  <div class="text-center main">
  <v-row>
    <v-container class="con">
      <div >
      <v-img class="img" style="text-align:center"  src= "../assets/images/ico.png" alt="icooo">

      </v-img>
      </div>

      <h3 class="please">Please login to your account</h3>
      
  <br>
 <v-form
   class="form"
    ref="form"
    v-model="valid"
    lazy-validation
  >
    
  
          <v-text-field
          class="user flat"
            v-model="username"
            
      :rules="usernameRules"
      label="Username"
      required
      solo
          ></v-text-field>
      

 
  
          <v-text-field
          class="pass"
           v-model="password"
      :rules="passwordRules"
      label="Password"
      required
      solo
          ></v-text-field>
      
    

    <v-btn
      :disabled="!valid"
      
      class="mr-4 login "
      @click="validate"
    >
     <p class="lognow"> LOGIN NOW</p>
    </v-btn>

    <p class="forgot">Forgot your password?</p>
  </v-form>
      
    </v-container>
    </v-row>
  </div>
</template>

<script>


export default {
  
  data(){
    return{
     items:{
      src: require("../assets/images/ico.png"),
      },
   valid: true,
      username: '',
      usernameRules: [
        v => !!v || 'Userame is required',
        
      ],
      password: '',
      passwordRules: [
        v => !!v || 'Password is required',
       
      ],
     
     
    }
  },

    methods: {
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      },
      
    }
  }


    
  

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap');

.login{
  text-align: center !important;
  margin-top: 20px;
  
 width: 406px !important;
  height: 56px !important;
  object-fit: contain;
  border-radius: 14px;
  background-image: linear-gradient(98deg, #fb7f3e, #fa496e);
  
}
.lognow{
  margin-top: 15px;
  width: 99px !important;
  height: 26px !important;
  font-family: Montserrat;
  font-size: 16px !important;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.63;
  letter-spacing: normal;
  text-align: center;
  color: #ffffff
}

.user
{

  margin-top: 30px;
   margin-left: 280px !important;
   width: 466px;
  height: 56px;
  border-radius: 9px;
  background-color: #f4f4f6 !important;
}
.pass{
  margin-top: 15px !important;
 margin-left: 280px !important;
   width: 466px;
  height: 56px;
  border-radius: 9px;
  background-color: #f4f4f6 !important;
}
.con{
 margin-top: 60px !important;
   width: 1060px !important;
  height: 780px !important;
  border-radius: 10px;
  box-shadow: 3px 10px 26px 0 rgba(0, 0, 0, 0.08);
  background-color: #ffffff;
  text-align: center !important;
  
}

.forgot{
  margin-top: 30px;
  margin-left: 420px;
  width: 178px !important;
  height: 22px !important;
  
  font-size: 16px !important;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.38;
  letter-spacing: normal;
  text-align: center;
  color: #0095c4;
}

.main{
   width: 1440px !important;
  height: 900px !important;
  background-color: #f4f4f6;
}

.please{
 margin-left: 320px;
   margin-top: 90px !important;
    width: 400px ;
  height: 34px;
  font-family: Montserrat !important;
  font-size: 26px !important;
  font-weight: bold;
 
  line-height: 1.31;
  letter-spacing: normal;
 
  color: var(--dark);
}
.img{ 
  text-align: center !important;
  margin-top: 50px;
 margin-left: 450px;
   width: 78px;
  height: 79px;
}
 

 @media screen and (max-width:1200px ){
   .main{
     width: 100%;
   }
 }

 @media screen and (max-width:1200px ){
   .please{
     width: 50%;
     margin-left: 200px;
   }
 }
 @media screen and (max-width:1200px ){
   .user{
     width: 50%;
     margin-left: 200px !important;
   }
 }
  @media screen and (max-width:1200px ){
   .pass{
     width: 50%;
     margin-left: 200px !important;
   }
 }
 @media screen and (max-width:1200px ){
   .login{
     width: 50%;
     margin-left: -25px !important;
   }
 }
  @media screen and (max-width:1200px ){
   .forgot{
     width: 50%;
     margin-left: 340px !important;
   }
 }
  @media screen and (max-width:1200px ){
   .img{
     width: 10%;
     margin-left: 370px !important;
   }
 }
  @media screen and (max-width:960px ){
   .con{
     width: 50%;
    
   }
 }
 @media screen and (max-width:960px ){
   .please{
     width: 50%;
     margin-left: 220px !important;
    
   }
 }
  @media screen and (max-width:960px ){
   .user{
     width: 50%;
     margin-left: 240px !important;
    
   }
 }

  @media screen and (max-width:960px ){
   .pass{
     width: 50%;
     margin-left: 240px !important;
    
   }
 }
 
  @media screen and (max-width:960px ){
   .forgot{
     width: 50%;
     margin-left: 420px !important;
    
   }
 }

  @media screen and (max-width:960px ){
   .img{
     width: 10%;
     margin-left: 420px !important;
    
   }
 }
</style>
