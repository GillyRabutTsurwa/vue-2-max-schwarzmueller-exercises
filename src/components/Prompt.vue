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
      <li>Hook up the button to toggle the display of the two paragraphs. Use both v-if and v-show and inspect the elements to see the difference</li>
      <li>Output an unordered list of array elements of your choice. Also print the index of each element</li>
      <li>
        Print all key-value pairs of the following object:
        <strong>
          <em>{title: "Bible", author: "God", books: 66}</em>. Also print the index of each item
        </strong>
      </li>
      <li>
        Print the following object (only the values) and also create a nested loop for the array:
        <strong>
          <em>{name: 'TESTOBJECT', data: [1.67, 1.33, 0.98, 2.21]}</em>
        </strong>
        (hint: use v-for and v-if to achieve this)
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  name: "Prompt",
  data() {
    return {
      title: "Conditionals & Loops with Lists"
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