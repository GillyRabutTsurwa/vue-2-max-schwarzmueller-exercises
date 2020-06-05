<template>
  <div>
    <div>
      <button @click="isShowing = !isShowing" class="btn">Show First</button>
      <button @click="isShowing2 = !isShowing2" class="btn">Show Second</button>
      <p v-if="isShowing">Toggle Me</p>
      <p v-if="isShowing2">Toggle me as well... But how am I different?</p>
    </div>
    <div>
      <h4>List of CSS & JS Frameworks</h4>
      <ul>
        <li
          v-for="(currentFramework, index) in frameworks"
          v-bind:key="index"
        >{{currentFramework}} - {{index + 1}}</li>
      </ul>
    </div>
    <div>
      <ul>
        <li v-for="(currentValue, propertyName, index) in myObject" v-bind:key="currentValue.id">
          <strong>{{index + 1}}</strong>
          - {{propertyName}}: {{currentValue}}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isShowing: false,
      isShowing2: false,
      frameworks: [
        "Vue",
        "Svelte",
        "React",
        "Angular",
        "Bulma",
        "Bootstrap",
        "Materialize",
        "UI-Kit",
        "Semantic UI"
      ],
      array: ["Max", "Anna", "Chris", "Manu"],
      myObject: {
        title: "Bible",
        author: "God",
        books: "66",
        // TESTING:
        id: 1
      },
      testData: {
        name: "TESTOBJECT",
        id: 10,
        data: [1.67, 1.33, 0.98, 2.21]
      }
    };
  },
  methods: {}
};
</script>

<style>
#effect {
  width: 100px;
  height: 100px;
  border: 1px solid black;
}
</style>