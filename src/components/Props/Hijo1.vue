
    <script setup>
import { ref } from 'vue'

defineProps({
  edad: String,
})

const count = ref(0)
</script>

<template>
  <h6 class="text-center">Soy el Oso hijo</h6>
  <p class="text-center">{{ edad }}</p>
</template>

<style scoped>

</style>

