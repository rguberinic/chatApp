<template>
  <div id="main">
    <app-online-users-side-bar />
    <app-main-chat-window />
    <app-user-profile-side-bar />
  </div>
</template>

<script>
import MainChatWindow from "../components/MainChatWindow";
import UserProfileSideBar from "../components/UserProfileSideBar";
import OnlineUsersSideBar from "../components/OnlineUsersSideBar";

export default {
  components: {
    "app-main-chat-window": MainChatWindow,
    "app-user-profile-side-bar": UserProfileSideBar,
    "app-online-users-side-bar": OnlineUsersSideBar
  }
};
</script>

<style scoped>
#main {
  width: 75vw;
  height: 80vh;
  border: 1px solid #f8f9fc;
  border-radius: 15px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}
</style>