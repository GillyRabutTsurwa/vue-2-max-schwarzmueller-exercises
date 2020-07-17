<template>
  <div>
    <h1>Exercise 4: {{title}}</h1>
    <p>
      I am doing these exercises knowing
      <strong>
        <em>alot</em>
      </strong> more about VueJS. Also, I am refreshing my fundamental skills using Vue2, but anything that is not in Vue3, I will skip those altogether for now
    </p>
    <p>
      Divide the code (that will be commented out but on this file) in to its separate components. I already added the bootstrap file so it should look decent.
      <!-- 
        <template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <header>
                    <h1>Server Status</h1>
                </header>
            </div>
        </div>
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-6">
                <ul class="list-group">
                    <li
                            class="list-group-item"
                            v-for="index in 5">
                        Server #{{ index }}
                    </li>
                </ul>
            </div>
            <div class="col-xs-12 col-sm-6">
                <p>Server Details are currently not updated</p>
            </div>
        </div>
        <hr>
        <div class="row">
            <div class="col-xs-12">
                <footer>
                    <p>All Servers are managed here</p>
                </footer>
            </div>
        </div>
    </div>
</template>
       -->
    </p>
    <h3>Treat the Tasks component like the primary App component. Tout commence de là</h3>
  </div>
</template>

<script>
export default {
  name: "Prompt",
  data() {
    return {
      title: "Components"
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