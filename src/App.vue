<template>
  <Top @RenderPublicarVaga="changeComponentToRenderize($event)" @RenderHome="changeComponentToRenderize($event)" ></Top>

  <component 
  :is="conteudo"
  >
  </component>

</template>

<script>

import Top from './components/layouts/Top.vue'
import Content from './components/layouts/Content.vue'
import Home from '@/components/views/Home.vue'
import PublicarVaga from '@/components/views/PublicarVaga.vue'

export default {
  name: 'App',
  components: {
    Top,
    Content,
    Home,
    PublicarVaga,
  },
  methods: {
    changeComponentToRenderize(e){
      this.conteudo = `${e.ComponentToRender}`
    }
  },
  data: () => ({
    conteudo: 'Home'
  })
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
