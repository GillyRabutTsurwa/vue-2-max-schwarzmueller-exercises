<template>
  <div>
    <div class="task-1">
      <span>First:</span>
      <button v-on:click="showAlert" class="btn">Click Me</button>
    </div>
    <div class="task-2">
      <span>Second:</span>
      <!-- pour que $event fasse plus de sens, considérer la suivante...
      disons que l'entrée a une id de pinchi...
      const inputPinchi = document.getElementById("pinchi");
      OK. Regardez bien.
      inputPinchi.addEventListener("keydown", (event) => {
        console.log(event.target.value) <== exactement ce que fait le méthode showInputValue. Mais avec Vue, c'est plus court est plus élégante, mais il faut des temps pour s'habituer à la syntaxe.
      })
      -->
      <input type="text" v-on:keydown="showInputValue($event)" placeholder="Type Here" />
      <p>{{inputValue}}</p>
    </div>
    <div class="task-3">
      <span>Third:</span>
      <!-- 
        L'efficacite de cette syntaxe s'affiche de plus lorsqu'on ajoute le modificateur de l'evenement ".enter", avec le JavaScript regulier, il nous faudrait utiliser une phrase if pour verifier que la boutton "enter" a été appuyé
      -->
      <input type="text" v-on:keydown.enter="showInputValueOnEnter($event)" placeholder="Type Here" />
      <p>{{inputValueOnEnter}}</p>
    </div>
    <hr />
    <div class="bonus-task">
      <p>
        Values of Input are fetched by
        <strong>two-way data binding</strong>
      </p>
      <form v-on:submit.prevent="logInfo">
        <input type="text" class="bonus-task__text" placeholder="Fill Your Name" v-model="formName" />
        <input
          type="number"
          class="bonus-task__number"
          placeholder="Fill Your Age"
          v-model="formAge"
        />
        <button type="submit" class="btn">Submit Info</button>
      </form>
    </div>
    <div class="bonus-task-2">
      <div class="square" v-on:mousemove="fetchCoordinates($event)">{{x}}, {{y}}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputValue: "",
      inputValueOnEnter: "",
      // // // // // // // // //
      formName: "",
      formAge: null,
      // // // // // // // // //
      x: 0,
      y: 0
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
    },
    logInfo() {
      console.log(this.formName);
      console.log(this.formAge);
    },
    fetchCoordinates(e) {
      this.x = e.offsetX;
      this.y = e.offsetY;
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

.bonus-task__text,
.bonus-task__number {
  display: block;
  margin: 0.75em auto;
}

.square {
  display: flex;
  justify-content: center;
  align-items: center;
}

.square {
  width: 300px;
  height: 300px;
  background-color: #2a2a2a;
  color: #fff;
}
</style>