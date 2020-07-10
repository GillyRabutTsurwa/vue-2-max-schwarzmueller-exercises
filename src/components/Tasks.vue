<template>
  <div>
    <button @click="value++" class="btn">Add 1</button>
    <button @click="value+=5" class="btn">Add 5</button>
    <p>{{value}} - {{printResult}}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value: 0,
      result: ""
    };
  },
  computed: {
    printResult() {
      return this.value < 20
        ? "Not there Yet"
        : this.value > 30
        ? "Woah... Cool it... We're going to get you back to zero"
        : "You at the sweetspot";
    }
  },
  watch: {
    //NOTE: notice how the name of this function is the same as the value we want to watch over (look up at data)
    value: function() {
      var vm = this;
      if (vm.value > 30) {
        setTimeout(() => {
          vm.value = 0;
        }, 5000);
      }
    }
  }
};
</script>

<style>
</style>