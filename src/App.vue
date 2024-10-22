<template>
  <globalHeader />
  <div id="app">
    <router-view />
  </div>
</template>

<script setup>
import globalHeader from '@/components/global/header.vue'
</script>

<script>
import { useHead } from '@vueuse/head'

useHead({
  script: [
    {
      src: 'https://kit.fontawesome.com/610163c2e2.js',
      crossorigin: 'anonymous',
    },
  ],
})
</script>

<style lang="scss">
body {
  font-family: 'Roboto', sans-serif;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0px 25px;
}
</style>
