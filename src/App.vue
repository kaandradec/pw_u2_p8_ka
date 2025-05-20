<template>
  <!-- <ContadorView></ContadorView> -->
  <ProductoView />
</template>

<script>
// import ContadorView from "@/views/ContadorView.vue";
// import EstudianteTablaView from "@/views/EstudianteTablaView.vue";
import ProductoView from "@/views/ProductoView.vue";

export default {
  name: "App",
  components: {
    // ContadorView,
    ProductoView,
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
