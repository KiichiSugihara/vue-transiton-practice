<template>
  <div id="app">
    <img width="25%" src="./assets/logo.png">
    <HelloWorld msg="Hello Vue in CodeSandbox!"/>
    <button @click="isShown =!isShown">表示の切り替え</button>
    <transition>
      <p v-show="isShown">HELOO!!!</p>
    </transition>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",
  components: {
    HelloWorld
  },
  data: function() {
    return {
      isShown: false
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.v-enter-active,
.v-leave-active {
  transition: opacity 500ms ease-out;
}

.v-enter {
  opacity: 0;
}

.v-enter-to {
  opacity: 1;
}

.v-leave {
  opacity: 0;
}

.v-leave-to {
  opacity: 1;
}
</style>
