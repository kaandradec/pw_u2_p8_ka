<template>
  <HolaMundoVue></HolaMundoVue>
</template>

<script>
import HolaMundoVue from "./views/HolaMundoView.vue";

export default {
  name: "App",
  components: {
    HolaMundoVue,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
