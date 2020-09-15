<template>
  <div id="input_bar_container">
    <div id="input_button_control">
      <input type="text">
      <button>Submit</button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
#input_bar_container {
  width: 100%;
  height: 10%;
  display: flex;
  align-items: center;
  justify-content: center;
  border-top: 1px solid #f8f9fc;
}

#input_button_control {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

#input_button_control input {
  width: 50%;
}

#input_button_control button {
  width: 3.5vw;
  font-size: 0.8vw;
  text-align: center;
}
</style>