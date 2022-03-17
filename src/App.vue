<template>
  <div id="app">
    <HeaderVue/>
    <MainVue/>
  </div>
</template>

<script>

import HeaderVue from './components/HeaderComponent.vue'
import MainVue from './components/MainComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderVue,
    MainVue
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
