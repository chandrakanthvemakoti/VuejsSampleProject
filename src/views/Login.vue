<template>

  <v-container fluid class="top">

  <v-row>
    <col cols="12">
    <v-container>
    <div class="middle"  >
      <v-form 
       ref="form"
    v-model="isValid"
    lazy-validation>

   <v-row justify="center">
     <v-col cols="6" sm="3"  md="2" class="text-center">
       
       <v-img class="image mt-12 ml-8 " src="../assets/images/ico.png">

       </v-img>


     </v-col>
   </v-row>
   <v-row justify="center">
     <v-col cols="10" sm="6" md="5" offset-md="1" offset-sm="1">

    <h3 class="please ml-n4 mt-12">Please login to your account</h3>

     </v-col>

   </v-row>

   <v-row justify="center">
     <v-col cols="11" sm="6" md="5" class="text-center">
       <v-text-field
       class="user"
        v-model="username"
          :rules="usernameRules"
            label="Username"
            outlined
            solo
            required
           
          ></v-text-field>
     </v-col>
   </v-row>
   
    <v-row justify="center">
     <v-col cols="11" sm="6" md="5" class="text-center">
       <v-text-field
       class="pass mt-n6"
            label="Password"
            v-model="password"
        type="password"
        :rules="passwordRules"
        required
            outlined
            solo
           
          ></v-text-field>
     </v-col>
   </v-row>

   <v-row justify="center">
   <v-col cols="11" sm="6" md="4">
      <v-btn
       :disabled="!isValid"
       block x-large
       @click="validate"
      
       class="login mt-n6"><p class="logtext mt-4" >Login now</p></v-btn>

   </v-col>
   </v-row>
   
  <v-row justify="center">
    <v-col cols="8" sm="4" md="3" >
      <p class="forgot" type="button">Forgot your password?</p>
    </v-col>

  </v-row>
      </v-form>
    </div>

</v-container>
  </v-row>


  </v-container>

</template>

<script>
export default {


  data(){
    return{
     
   isValid: true,
      username: '',
      usernameRules: [
        v => !!v || 'Username is required',
        
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
    }
  }

  

</script>

<style scoped>
 @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap');
.top{
 
  background-color: #f4f4f6;
  width: 100%;
  height: 100%;
}
.middle{
   margin-top:30px;
   width: 100%;
  height: 780px;
  border-radius: 10px;
  box-shadow: 3px 10px 26px 0 rgba(0, 0, 0, 0.08);
  background-color: #ffffff;
}
.image{
   width: 80px;
  height: 80px;
}
.please{
  
  font-family: Montserrat;
  font-size: 26px;
  font-weight: bold;
}
.user{
 
  border-radius: 9px;
}
.pass{
 
  border-radius: 9px;
}
.login{
height: 56px !important;
border-radius: 14px;
  
  background-image: linear-gradient(98deg, #fb7f3e, #fa496e);
}

.logtext{
  width: 99px;
  height: 26px;
  font-family: Montserrat;
  font-size: 16px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.63;
  letter-spacing: normal;
  text-align: center;
  color: #ffffff;
}
.forgot{
 
 
  font-size: 18px !important;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.38;
  letter-spacing: normal;
  text-align: center;
  color: #0095c4;
}
 @media screen and (max-width:860px){
   .middle {
     margin-top:-30px !important ;
     
   }
 }





/* @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@800&display=swap');

.top{
  background-color: #f4f4f6;
  width: 100%;
  height: 900px;
}
.middle{
   margin-top: 30px;
  width: 100%;
  height: 780px;
  border-radius: 10px;
  box-shadow: 3px 10px 26px 0 rgba(0, 0, 0, 0.08);
  background-color: #ffffff;
}
.image{
  width: 80px;
  height: 80px;
}

.login{
 
  height: 56px !important;
 
  
  background-image: linear-gradient(98deg, #fb7f3e, #fa496e);
}


.user{
  width: 466px !important;
  height: 56px !important;
  border-radius: 9px;
  
}


.pass{
  width: 466px !important;
  height: 56px !important;
  border-radius: 9px;

}

.forgot{

  width: 178px !important;
  height: 22px !important;
  margin-left: 140px;
  font-size: 18px !important;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.38;
  letter-spacing: normal;
  text-align: center;
  color: #0095c4;
}

.logtext{

  width: 99px;
  height: 26px;
  font-family: Montserrat;
  font-size: 16px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.63;
  letter-spacing: normal;
  text-align: center;
  color: #ffffff;

}
 .please{
 margin-left: 230px;
  display: inline;
 
  font-family: Montserrat;
  font-size: 26px;
  font-weight: bold;

 }



















@media screen  and (max-width:800px ){
  .middle{
    margin: 0%;
    height: 100% !important;
  }
  
}

@media screen  and (max-width:1260px ){
  .please{
    
    margin-left: 130px;
  }
  
}

@media screen  and (max-width:960px ){
  .please{
    
    margin-left: 250px;
  }
  
}
 @media screen  and (max-width:860px ){
  .please{
     width: 100%;

    margin-left: 200px;
  }
  
}
@media screen  and (max-width:760px ){
  .please{
   margin-left: 150px;
  }
  
}

@media screen  and (max-width:660px ){
  .please{
   margin-left: 110px;
   
  }
  
}
@media screen  and (max-width:560px ){
  .please{
  
   display: inline-block;
  }
  
}


@media screen  and (max-width:600px ){
  .please{
   margin-left: 20px;
  }
  
}

 @media screen  and (max-width:600px ){
  .user{
    
    width: 100% !important;

  }
  
}
@media screen  and (max-width:600px ){
  .forgot{
    margin-left: 120px;
    width: 100% !important;
  }
  
}


 @media screen  and (max-width:600px ){
  .pass{
    
    width: 100% !important;
  }
  
}

@media screen  and (max-width:600px ){
  .forgot{
    margin-left: 180px !important;
    width: 100% !important;
  }
  
}
@media screen  and (max-width:1260px ){
  .forgot{
    margin-left: 80px;
    width: 100% !important;
  }
  
}
@media screen  and (max-width:960px ){
  .forgot{
    margin-left: 220px;
    width: 100% !important;
  }
  
}

@media screen  and (max-width:860px ){
  .forgot{
    margin-left: 160px;
    width: 100% !important;
  }
  
}

@media screen  and (max-width:760px ){
  .forgot{
    margin-left: 120px;
    width: 100% !important;
  }
  
}
@media screen  and (max-width:660px ){
  .forgot{
    margin-left: 120px;
    width: 100% !important;
  }
  
}

@media screen  and (max-width:560px ){
  .forgot{
    margin-left: 140px !important;
    width: 100% !important;
  }
  
}
@media screen  and (max-width:460px ){
  .forgot{
    margin-left: 100px !important;
    width: 100% !important;
  }
  
}

@media screen  and (max-width:360px ){
  .forgot{
    margin-left: 70px !important;
    width: 100% !important;
  }
  
}
 
 */

</style>