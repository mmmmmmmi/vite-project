<script setup>
import { ref } from 'vue'

defineProps({
  msg: String
})

const count = ref(0)
const env = import.meta.env
</script>

<template>
  <h1>{{ msg }}</h1>
  <p>运行模式<a>{{env.MODE}}</a></p>
  <p>部署应用时基本URL<a>{{env.BASE_URL}}</a></p>
  <p>应用是否运行在生产环境<a>{{env.PROD}}</a></p>
  <p>应用是否运行在开发环境<a>{{env.DEV}}</a></p>
  <p>Some Key <a>{{env.VITE_SOME_KEY}}</a></p>
  <p>
    Recommended IDE setup:
    <a href="https://code.visualstudio.com/" target="_blank">VSCode</a>
    +
    <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>
  </p>

  <p>
    <a href="https://vitejs.dev/guide/features.html" target="_blank">
      Vite Documentation
    </a>
    |
    <a href="https://v3.vuejs.org/" target="_blank">Vue 3 Documentation</a>
  </p>

  <button type="button" @click="count++">count is: {{ count }}</button>
  <p>
    Edit
    <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>
</template>

<style scoped lang="scss">
p{
  color: black;
  a{
    color: #42b983
  }
}

</style>
