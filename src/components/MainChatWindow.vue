<template>
  <div id="chat_window">
    <h1>Chat app title</h1>
    <app-chat-container />
    <app-input-bar-container />
  </div>
</template>

<script>
import ChatContainer from "../components/ChatContainer";
import InputBarContainer from "../components/InputBarContainer";
export default {
  components: {
    "app-chat-container": ChatContainer,
    "app-input-bar-container": InputBarContainer
  }
};
</script>

<style scoped>
#chat_window {
  width: 50%;
  height: 100%;
  border-left: 1px solid #f8f9fc;
  border-right: 1px solid #f8f9fc;
  background-color:#fff
}

#chat_window > h1 {
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