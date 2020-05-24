<template>
  <div>
    <h1>Exercise 3: {{title}}</h1>
    <p>
      I am doing these exercises knowing
      <strong>
        <em>alot</em>
      </strong> more about VueJS. Also, I am refreshing my fundamental skills using Vue2, but anything that is not in Vue3, I will skip those altogether for now
    </p>
    <ol>
      <li>Show a "result" of 'not there yet' as long as "value" is not equal to 37 - you can change "value" with the buttons. Print 'done' once you did it</li>
      <li>Watch for changes in the "result" and reset the "value" after 5 seconds (hint: setTimeout(..., 5000)</li>
    </ol>
  </div>
</template>

<script>
export default {
  name: "Prompt",
  data() {
    return {
      title: "Computed & Watch"
    };
  }
};
</script>

<style>
li {
  width: 50%;
  text-align: left;
}
</style>