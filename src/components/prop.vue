<script setup>
const props = defineProps({
  lists: {
    type: Array,
    default: () => []
  }
})
</script>

<template>
  <ul>
    <li v-for="(list, index) in props.lists" :key="index">{{ list }}</li>
  </ul>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
