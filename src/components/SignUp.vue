<template>
  <div id="signup">
    <h2>Please Sign up</h2>
    <input
      type="text"
      placeholder="enter your email"
      v-model="email"
    >
    <input
      type="text"
      placeholder="choose username"
      v-model="username"
    >
    <input
      type="text"
      placeholder="choose password"
      v-model="password"
    >
    <input
      type="text"
      placeholder="repeat password"
      v-model="password2"
    >
    <button @click="signUp">Signup</button>
    <p>Already a member?</p>
    <button @click="toggleSignUp">Log in</button>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data(){
    return {
      email:"",
      username:"",
      password:"",
      password2:""
    }
  },
  methods: {
    toggleSignUp() {
      this.$emit("toggleSignUp");
    },
    signUp() {
      console.log(this.email,this.username,this.password,this.password2)
      axios.post('http://097a122.e2.mars-hosting.com/praksa_2020_septembar/api/auth/signup', {
        email:this.email,
        username:this.username,
        password:this.password,
        password2:this.password2
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

<style>
#signup{
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 90%;
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