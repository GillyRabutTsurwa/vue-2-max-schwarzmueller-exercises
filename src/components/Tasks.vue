<template>
  <div class="container">
    <Tete />
    <hr>
    <Server />
    <!-- <ServerInfo /> -->
    <hr>
    <Pied />
  </div>
</template>

<script>
import Header from "./Header";
import Server from "./Server";
// import ServerInfo from "./ServerInfo";
import Footer from "./Footer";
export default {
  name: "Tasks",
  components: {
    Tete: Header,
    Server: Server,
    // ServerInfo: ServerInfo,
    Pied: Footer
  }
};
</script>

<style>
</style>