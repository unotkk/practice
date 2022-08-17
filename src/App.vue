<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from './components/HelloWorld.vue'
import PropCmpt from './components/prop.vue'
import emit from './components/emit.vue'
import { ref } from 'vue'
const lists = ref(['HTML', 'JAVASCRIPT', 'CSS'])
const val = ref('')
const add = () => {
  lists.value.push(val.value)
  val.value = ''
}
const addList = val => {
  lists.value.push(val)
}
</script>

<template>
  <!-- <div>
    <input type="text" v-model="val">
  </div>
  <button type="submit" @click="add">button</button>
  <PropCmpt :lists="lists"/> -->
  <!-- <HelloWorld msg="Vite + Vue" /> -->
  <ul>
    <li v-for="item in lists" :key="item">{{ item }}</li>
  </ul>
  <emit @add="addList" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
