<script setup>
const name = "Vue dinamico";
const styleColor = "color: blue";
const activo = false;
const gay = true;
const arrayFrutas = [
  {
    name: "Manzana",
    price: "$1.00",
    description: "Una manzana",
  },
  {
    name: "Pera",
    price: "$2.00",
    description: "Una pera",
  },
  {
    name: "Naranja",
    price: "$3.00",
    description: "Una naranja",
  },
];
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <h2 :style="styleColor">Soy azul gracias a v-bind</h2>
  <h2>
    {{ activo ? "Estoy activo" : "Me fui a la verga" }}
  </h2>
  <p v-if="gay">Soy Gay</p>
  <p v-if="!gay">No soy Gay</p>
  <p>{{ arrayFrutas }}</p>
  <p>{{ arrayFrutas[1] }}</p>
  <h2>Lista de frutas</h2>
  <ul>
    <li v-for="(fruta, index) in arrayFrutas" :key="index">
      {{ index }} - {{ fruta }}
    </li>
  </ul>
</template>

<style>
h1 {
  color: red;
}
</style>
