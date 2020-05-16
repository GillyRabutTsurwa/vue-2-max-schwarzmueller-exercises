<template>
  <div>
    <h1>Exercise 2: {{title}}</h1>
    <p>
      I am doing these exercises knowing
      <strong>
        <em>alot</em>
      </strong> more about VueJS. Also, I am refreshing my fundamental skills using Vue2, but anything that is not in Vue3, I will skip those altogether for now
    </p>
    <ol>
      <li>Show an alert when the Button gets clicked</li>
      <li>Listen to the "keydown" event and store the value in a data property (hint: event.target.value gives you the value)</li>
      <li>Adjust the example from #2 to only fire if the "key down" is the ENTER key</li>
    </ol>
  </div>
</template>

<script>
export default {
  name: "Prompt",
  data() {
    return {
      title: "Events"
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