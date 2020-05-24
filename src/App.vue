<template>
  <div id="app">
    <img class="logo" alt="Vue logo" src="./assets/logo.png" />
    <Prompt />
    <hr />
    <Methods />
    <Computed />
    <button @click="clearConsole" class="btn">Clear Console</button>
    <hr />
    <h3>Now for the Tasks</h3>
    <Tasks />
  </div>
</template>

<script>
import Prompt from "./components/Prompt";
import Methods from "./components/MethodsEg";
import Computed from "./components/ComputedEg";
import Tasks from "./components/Tasks";

export default {
  name: "App",
  components: {
    Prompt: Prompt,
    Methods: Methods,
    Computed: Computed,
    Tasks: Tasks
  },
  methods: {
    //NOTE: just a method to clear the console.
    clearConsole() {
      console.clear();
      location.reload();
      return false;
    }
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

.logo {
  position: fixed;
  top: 2em;
  left: 2em;
  width: 3em;
  height: 3em;
}

.btn {
  cursor: pointer;
  outline: none;
  border: 0.1em solid transparent;
  font-size: 1.1em;
  padding: 0.7em 1.1em;
  margin: 1em;
  text-transform: uppercase;
  background-color: #42b883;
  color: #fff;
  font-weight: 600;
  border-radius: 0.5em;
  transition: all 0.2s ease-in;
}

.btn:hover {
  color: #42b883;
  background-color: #fff;
  border: 0.1em solid #42b883;
}
</style>
