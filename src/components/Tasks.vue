<template>
  <div>
    <!-- NOTE: The value of a bound class (like toggleClass) is ALWAYS an object. The property is the name of the class and the value is a true or false values that determines if the class will be implemented. This object can be made inline or in the JavaScript. -->
    <div v-bind:class="toggleClass">
      <p>Pinchi ma pinchi</p>
    </div>
    <button @click="startEffect" class="btn">Start Effect</button>
    <!-- NOTE: Okay so what I said above is not necessarily true. Je veux dire que: we can also use arrays. In this case, the value of the bound class (arrayClasses) is an array of the classes (which are strings) defined in the CSS -->
    <p v-bind:class="arrayClasses">Array of classes pinchi</p>
    <!-- NOTE: Voilà ce que j'ai fait...
    Each time we press enter on the input, we run the addClass() which addes a class to the array inputArrayClasses. 
    We use attach the variable addClassName to be the value of the input using two-way binding and add this value to the inputArrayClasses, again, using the addClass()-->
    <input
      type="text"
      @keyup.enter="addClass"
      v-model="addedClassName"
      placeholder="Enter Class Names"
    />
    <p>{{addedClassName}}</p>
    <h4 v-bind:class="inputArrayClasses">Les classes m'ajoutent via l'entrée dessûs (input)</h4>
    <!--  -->
    <input
      type="text"
      @keyup.enter="addColour"
      v-model="inputColour"
      placeholder="Enter Colour Names"
    />
    <h4 v-bind:style="colourObj">Les styles m'ajoutent via l'entrée dessûs ma pinchi</h4>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // Toggle class is the object declared in the template
      toggleClass: {
        // Highlight and shrink are CSS classnames, go to CSS for proof;
        highlight: true,
        shrink: false
      },
      // Array of classes. Classes are written as strings.
      arrayClasses: ["arrayClass1", "arrayClass2", "arrayClass3"],
      // variable responsible for adding classnames to the inputArrayClasses array.
      addedClassName: "",
      // array of classes. Classes are added using the input value addClassName
      inputArrayClasses: [],
      inputColour: "",
      /////////////////////////////////////
      colourObj: {
        color: ""
      }
    };
  },
  methods: {
    // This method just toggles the classes between each other;
    startEffect() {
      setInterval(() => {
        this.toggleClass.highlight = !this.toggleClass.highlight;
        this.toggleClass.shrink = !this.toggleClass.shrink;
      }, 3000);
    },
    addClass() {
      if (this.addedClassName === "") this.inputArrayClasses = [];
      this.inputArrayClasses = [...this.inputArrayClasses, this.addedClassName];
    },
    addColour() {
      this.colourObj.color = this.inputColour;
    }
  }
};
</script>

<style>
#effect {
  width: 100px;
  height: 100px;
  border: 1px solid black;
}

.highlight {
  background-color: red;
  width: 200px !important;
}

.shrink {
  background-color: gray;
  width: 50px !important;
}

.arrayClass1 {
  color: forestgreen;
}
.arrayClass2 {
  text-transform: uppercase;
}
.arrayClass3 {
  font-size: 2em;
}
</style>