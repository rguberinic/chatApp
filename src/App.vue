<template>
  <div id="app">
    <app-nav />
    <router-view></router-view>
  </div>
</template>

<script>
import NavBar from "../src/components/NavBar";
export default {
  components: {
    "app-nav": NavBar
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@400;700;900&family=Raleway:wght@300;400;500&display=swap');

h1,h2,h3,h4,h5 {
  font-family: 'Lato', sans-serif;
}

p{
  font-family: 'Raleway', sans-serif;
}

* {
  box-sizing: border-box;
}

#app{
  height: 100%;
}

body {
  height: 100vh;
  margin: 0;
  padding: 0;
  background: #2193b0;  /* fallback for old browsers */
  background: -webkit-linear-gradient(to right, #6dd5ed, #2193b0);  /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(to right, #6dd5ed, #2193b0); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

}
</style>
