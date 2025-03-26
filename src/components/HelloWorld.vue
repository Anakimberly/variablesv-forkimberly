<script setup>
import { ref } from 'vue'
const bienvenida = ref("Bienvenidos a la seccion de condicionales")
const nombre = ref("Ana Kimberly")
const apellidos = ref ("Hernandez Perez")
//defineProps({
  //msg: String,
//})

const count = ref(0)
</script>

<template>
  <div class="container"></div>
  <h2 class="text-center"> {{ bienvenida }}</h2>
  <div class="row">
    <div class="col-md-6">
      <h6 class="">{{ nombre }}</h6>
      <h6>{{ apellidos }}</h6>
    </div>
  </div>
</template>

<style scoped>

</style>
