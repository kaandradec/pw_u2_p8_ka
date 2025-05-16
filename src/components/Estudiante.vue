<template>
  <div class="container">
    <label for="id_nombre">Nombre: </label>
    <!-- v-model: Vincular una entrada a una propiedad reactiva  -->
    <!-- Usa el patrón  de diseño modelo vista controlador -->
    <!-- 
     Vista: Parte visual, 
     Modelo: (Propiedad reactiva) Lo que viaja entre la vista y controlador, 
     Controlador: El JS se encarga de modificar los valores
     -->
    <input v-model="nuevoNombre" id="id_nombre" type="text" />

    <label for="id_apellido">Apellido: </label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" />
    <button v-on:click="agregarEstudiante()">Agregar Estudiante</button>
    {{ nuevoNombre }}
    <ul>
      <!-- v-for Directiva para y graficar componentes a partir de un arreglo o una lista -->
      <!-- <li v-for="estu in lista" :key="estu.nombre">
        Nombre: {{ estu.nombre }} - Apellido: {{ estu.apellido }}
      </li> -->

      <!-- Con desestructuración de objetos -->
      <li v-for="{ nombre, apellido } in lista" :key="nombre">
        Nombre: {{ nombre }} - Apellido: {{ apellido }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nuevoNombre: "Nuevo",
      nuevoApellido: "Nuevo Apellido",
      lista: [
        { nombre: "Kevin", apellido: "Andrade" },
        { nombre: "Daniel", apellido: "Vera" },
        { nombre: "Pedro", apellido: "Sanchez" },
        { nombre: "Jorge", apellido: "Teran" },
        { nombre: "Carlos", apellido: "Castillo" },
        { nombre: "Viviana", apellido: "Lopez" },
      ],
    };
  },
  methods: {
    agregarEstudiante() {
      const nuevoEst = {
        nombre: this.nuevoNombre,
        apellido: this.nuevoApellido,
      };
      //   this.lista.unshift(nuevoEst);
      this.lista.push(nuevoEst);
    },
  },
};
</script>

<style>
</style>