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
  <h2> {{ bienvenida }}</h2>
</template>

<style scoped>

</style>
