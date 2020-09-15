<template>
  <div id="user_profile_sidebar">
    <h3>User Info</h3>
    <div id="user_img_container">
      <img
        src="../assets/39013954-f5091c3a-43e6-11e8-9cac-37cf8e8c8e4e.jpg"
        alt="user_image"
      >
    </div>
    <p id="username">Name: Rade Guberinić</p>
    <p id="user_position">Title: Noob</p>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
#user_profile_sidebar {
  height: 100%;
  width: 25%;
  background-color: #f9f9f9;
}

#user_img_container {
  height: 10vh;
  width: 10vh;
  margin: 0 auto;
  border-radius: 100%;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 2%;
}

#user_img_container > img {
  width: 100%;
  height: 100%;
}

#user_profile_sidebar > p {
  text-align: center;
  font-weight: 500;
}

#user_profile_sidebar > h3 {
  margin: 0;
  width: 100%;
  height: 10%;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  font-size: 1.5vw;
  border-bottom: 1px solid #f8f9fc;
}
</style>