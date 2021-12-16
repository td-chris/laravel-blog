<template>
  <div id="app">
    <Navbar />
    <Artigos msg="Meus artigos"/>
  </div>
</template>

<script>
import Artigos from './components/Artigos.vue'
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Artigos,
    Navbar
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
}
</style>
