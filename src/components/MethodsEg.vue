<template>
  <div>
    <button @click="firstValue++" class="btn">Add 1</button>
    <button @click="secondValue += 5" class="btn">Add 5</button>
    <p>{{firstValue}}</p>
    <p>{{secondValue}}</p>
    <p>First value: {{addToFirst()}}</p>
    <p>Second value: {{addToSecond()}}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      age: 24,
      firstValue: 0,
      secondValue: 0
    };
  },
  //NOTEIMPORTANT: With methods, both methods run regardless of only one method needed to run upon click (use the log console to see thsi better). This is not efficient. This is where the computed property come in
  //NOTEIMPORTANT: Methods that return must have parantheses included in the declaration in the template. Computed properties do not need parantheses. Also, computed properties can't be writted as ES6 methods.
  methods: {
    addToFirst() {
      console.log("addToFirst method is running");
      return this.age + this.firstValue;
    },
    addToSecond() {
      console.log("addToSecond method is running");
      return this.age + this.secondValue;
    }
  }
};
</script>

<style>
</style>