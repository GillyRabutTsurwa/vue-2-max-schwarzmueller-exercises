<template>
  <div class="francais">
    <button @click="premiereValeur++" class="btn">Ajouter 1</button>
    <button @click="deuxiemeValeur += 5" class="btn">Ajouter 5</button>
    <p>{{premiereValeur}}</p>
    <p>{{deuxiemeValeur}}</p>
    <p>Première valeur: {{ajouterVersPremier}}</p>
    <p>Deuxième valeur: {{ajouterVersDeuxieme}}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      âge: 24,
      premiereValeur: 0,
      deuxiemeValeur: 0
    };
  },
  //NOTEIMPORTANT: With methods, both methods run regardless of only one method needed to run upon click (use the log console to see this better). This is not efficient. This is where the computed property come in
  //NOTEIMPORTANT: Methods that return must have parantheses included in the declaration in the template. Computed properties do not need parantheses. Also, computed properties can't be writted as ES6 methods.
  computed: {
    ajouterVersPremier: function() {
      console.log("La méthode ajouterVersPremier est en cours");
      return this.âge + this.premiereValeur;
    },
    ajouterVersDeuxieme: function() {
      console.log("La méthode ajouterVersDeuxieme est en cours");
      return this.âge + this.deuxiemeValeur;
    }
  }
};
</script>

<style>
</style>