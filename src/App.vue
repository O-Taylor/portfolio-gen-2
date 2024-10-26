<template>
  <div id="app">
    <globalHeader />
    <router-view />
    <globalFooter />
  </div>
</template>

<script setup>
import globalHeader from '@/components/global/header.vue'
import globalFooter from '@/components/global/footer.vue'
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
  background-color: #f9f9f9;
}

* {
  box-sizing: border-box;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0px 25px;
}
</style>
