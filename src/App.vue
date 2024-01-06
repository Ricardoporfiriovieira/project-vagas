<template>
  <Top></Top>
  <Content></Content>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

import Top from './components/layouts/Top.vue'

import Content from './components/layouts/Content.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Top,
    Content,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
