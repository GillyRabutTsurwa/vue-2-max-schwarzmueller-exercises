<template>
  <div class="row">
    <div class="col-xs-12 col-sm-6">
      <ul class="list-group">
        <li class="list-group-item" v-for="index in 5" v-bind:key="index">
          <CurrentServer />
        </li>
      </ul>
    </div>
    <ServerStatus />
  </div>
</template>

<script>
import CurrentServer from "./CurrentServer";
import ServerStatus from "./ServerStatus";
export default {
  name: "Server",
  components: {
    CurrentServer: CurrentServer,
    ServerStatus: ServerStatus
  }
};
</script>

<style>
</style>