<template>
  <div id="app">
    <NavBar></NavBar>
    <MainContent></MainContent>
  </div>
</template>

<script>
import NavBar from './components/NavigationBar.vue'
import MainContent from './components/MainContent.vue'

export default {
  name: 'App',
  components: {
    NavBar, 
    MainContent
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
  margin: 0px;
  height: 100%;
}
</style>
