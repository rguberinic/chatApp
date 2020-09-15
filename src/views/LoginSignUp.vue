<template>
  <div id="login_signup_container">
    <app-login
      v-if="!toggleFormBool"
      @toggleSignUp="toggleFormBool=!toggleFormBool"
    />
    <app-signup
      v-if="toggleFormBool"
      @toggleSignUp="toggleFormBool=!toggleFormBool"
    />
  </div>
</template>

<script>
import LogIn from "../components/LogIn";
import SignUp from "../components/SignUp";

export default {
  components: {
    "app-login": LogIn,
    "app-signup": SignUp
  },
  data() {
    return {
      toggleFormBool: false
    };
  }
};
</script>

<style>
#login_signup_container {
  width: 20vw;
  height: 50vh;
  border: 1px solid #f8f9fc;
  border-radius: 15px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  background-color:#f9f9f9
}

#login_signup_container input,
#login_signup_container button {
  display: block;
}



#login_signup_container input[type="checkbox"] {
  display: inline;
  width: 8%;
}
</style>