<template>
  <div>
    <h1>Exercise 4: {{title}}</h1>
    <p>
      I am doing these exercises knowing
      <strong>
        <em>alot</em>
      </strong> more about VueJS. Also, I am refreshing my fundamental skills using Vue2, but anything that is not in Vue3, I will skip those altogether for now
    </p>
    <ol>
      <li>Start the Effect with the Button. The Effect should alternate the "highlight" or "shrink" class on each new setInterval tick (attach respective class to the div with id "effect" below)</li>
      <li>Create a couple of CSS classes and attach them via the array syntax</li>
      <li>Let the user enter a class (create some example classes) and attach it</li>
      <li>Let the user enter a class and enter true/ false for another class (create some example classes) and attach the classes</li>
      <li>Repeat #3 but now with values for styles (instead of class names). Attach the respective styles. NOTE: Successful with colour, will add other styles in the future</li>
      <li>
        Create a simple progress bar with setInterval and style bindings. Start it by hitting the below button.
        <strong>
          <em>Not yet attempted</em>
        </strong>
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  name: "Prompt",
  data() {
    return {
      title: "Styling"
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