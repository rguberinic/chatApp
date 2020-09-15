<template>
  <div id="login">
    <h2>Welcome user, please log in</h2>
    <input
      type="text"
      placeholder="enter your email"
      v-model="email"
    >
    <input
      type="password"
      placeholder="enter your password"
      v-model="password"
    >
    <div id="remember_me">
      <span>Remember me</span>
      <input type="checkbox">
      
    </div>
    <button @click="logIn">Log in</button>
    <div id="signup_form">
      <p>Not a member?</p>
      <button @click="toggleSignUp">Sign up</button>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data(){
    return {
      email:"",
      password:""
    }
  },
  methods: {
    toggleSignUp() {
      this.$emit("toggleSignUp");
    },
    logIn(){
      axios.post('http://097a122.e2.mars-hosting.com/praksa_2020_septembar/api/auth/login', {
        email: this.email,
        password: this.password
      })
      .then(function (response) {
        console.log(response);
      })
      .catch(function (error) {
        console.log(error);
      });
    }
  }
  

};
</script>

<style scoped>
#login {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 90%;
}

#signup_form {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 100%;
}

#remember_me {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

input {
  margin: 4% 0;
  width: 100%;
  padding: 2%;
}

button {
  margin: 4% 0;
  width: 100%;
  padding: 1% 2%;
  background-color: #04809D;
  border:1px solid #a2bafa;
  color:#fff;
  font-size: 1vw;
  font-family: 'Raleway', sans-serif;
}

span {
  font-family: 'Raleway', sans-serif
}

h2 {
  color:#2193b0
}



</style>