<template>
  <Top @EventPublicarVaga="acao($event)" @EventHome="acao($event)" ></Top>
  <!-- <Content>
  </Content> -->
  <!-- <Home></Home> -->

  <component 
  :is="conteudo"
  >
  </component>

</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

import Top from './components/layouts/Top.vue'
import Content from './components/layouts/Content.vue'
import Home from '@/components/views/Home.vue'
import PublicarVagas from '@/components/views/PublicarVagas.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Top,
    Content,
    Home,
    PublicarVagas,
  },
  methods: {
    acao(e){
      this.conteudo = `${e.screen}`
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
