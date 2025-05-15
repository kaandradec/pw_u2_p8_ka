<template>
  <div class="container">
    <h1>Contador</h1>

    <p>{{ 10 }}</p>
    <!-- Muestra el número literal 10 -->
    <p>{{ 1 + 1 }}</p>
    <!-- Evalúa y muestra 2 -->
    <p>
      {{ numero }}<sup>2</sup> = {{ calCuadrado }}
      <!-- Muestra el valor de “numero” al cuadrado usando la propiedad computada -->
    </p>

    <div>
      <button v-on:click="incrementar()">+1</button>
      <button v-on:click="decrementar()">-1</button>
    </div>

    <!--
      Ejemplos adicionales (descomentarlos para ver funcionando):
        <p>{{ activo }}</p>              Muestra true o false
        <p>{{ usuario.edad }}</p>         Accede a una propiedad de un objeto
        <p>{{ arreglo }}</p>              Muestra el contenido de un array
        <p>{{ true ? 'Es Verdadero' : 'Es Falso' }}</p>
        <p>{{ false ? 'Es Verdadero' : 'Es Falso' }}</p>
    -->
  </div>
</template>

<script>
export default {
  // Función data(): define el estado reactivo del componente
  data() {
    return {
      numero: 5, // Valor inicial del contador
      texto: "Kevin Andrade", // Ejemplo de dato tipo string
      activo: true, // Ejemplo de dato booleano
      usuario: {
        // Objeto anidado con varias propiedades
        nombre: "Kevin",
        edad: 25,
        profesion: "Estudiante",
      },
      arreglo: ["Azul"], // Ejemplo de array en el estado
    };
  },
  methods: {
    calcularCuadrado() {
      console.log("Entró al método calcularCuadrado");
      // Retorna el cuadrado de “numero” (sin cachear)
      return this.numero * this.numero;
    },
    incrementar() {
      this.numero++;
    },
    decrementar() {
      this.numero--;
    },
  },
  // Computed: propiedades computadas con cache
  computed: {
    calCuadrado() {
      console.log("Entró a la propiedad computada calCuadrado");
      // Solo se recalcula cuando “numero” cambie; resultado cacheado
      return this.numero * this.numero;
    },
  },
};
</script>

<style>
h1 {
  color: rgb(128, 235, 128);
  background: rgb(83, 83, 238);
}

p {
  background: rgb(236, 236, 117);
}
</style>
