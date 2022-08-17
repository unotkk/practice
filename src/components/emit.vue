<script setup>
import { ref } from 'vue'
const val = ref('')
const emits = defineEmits(['add'])
const handleSubmit = () => {
  emits('add', val.value)
  val.value = ''
}
</script>

<template>
  <input type="text" v-model="val" />
  <hr />
  <button type="submit" @click="handleSubmit">+</button>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
