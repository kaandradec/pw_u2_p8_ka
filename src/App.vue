<template>
  <!-- <ContadorView></ContadorView> -->
  <EstudianteView />
</template>

<script>
// import ContadorView from "@/views/ContadorView.vue";
import EstudianteView from "@/views/EstudianteView.vue";

export default {
  name: "App",
  components: {
    // ContadorView,
    EstudianteView,
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
