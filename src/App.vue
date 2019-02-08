<template>
  <div id="app"><img width="25%" src="./assets/logo.png" /> <Tax /></div>
</template>

<script>
import Tax from "./components/Tax";

export default {
  name: "App",
  components: {
    Tax
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
