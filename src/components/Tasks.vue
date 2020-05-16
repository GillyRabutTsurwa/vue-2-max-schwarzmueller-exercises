<template>
  <div>
    <div class="task-1">
      <span>First:</span>
      <button v-on:click="showAlert" class="btn">Click Me</button>
    </div>
    <div class="task-2">
      <span>Second:</span>
      <input type="text" v-on:keydown="showInputValue($event)" placeholder="Type Here" />
      <p>{{inputValue}}</p>
    </div>
    <div class="task-3">
      <span>Third:</span>
      <input type="text" v-on:keydown.enter="showInputValueOnEnter($event)" placeholder="Type Here" />
      <p>{{inputValueOnEnter}}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputValue: "",
      inputValueOnEnter: ""
    };
  },
  methods: {
    showAlert() {
      alert("This button is unnecessarily polished");
    },
    showInputValue(e) {
      this.inputValue = e.target.value;
      console.log(this.inputValue);
    },
    showInputValueOnEnter(e) {
      this.inputValueOnEnter = e.target.value;
      console.log(this.inputValueOnEnter);
    }
  }
};
</script>

<style>
.image {
  display: block;
  width: 400px;
  height: 400px;
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