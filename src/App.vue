<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Intro msg="Welcome to Your Vue.js App" />
    <h3>Je vais revenir et pratiquer les basiques des basiques</h3>
  </div>
</template>

<script>
import Intro from "./components/Intro.vue";

export default {
  name: "App",
  components: {
    Intro: Intro
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
