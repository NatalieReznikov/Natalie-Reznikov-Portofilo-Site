<template>
  <div id="app">
    <nav-bar :activeID="activeID" :Slides="slides" @select="activeID = $event"></nav-bar>
    <main-content :activeID="activeID" @select="change_page($event)"></main-content>
  </div>
</template>

<script>
import NavBar from './components/NavigationBar.vue'
import MainContent from './components/MainContent.vue'

export default {
  name: 'App',
  data :  function() {
    return {
      activeID : 0,
      slides :
        [
          {
            id : 0,
            msg : 'Home Page'
          },
          {
            id : 1,
            msg : 'Bio'
          },
          {
            id : 2,
            msg : 'Publications'
          },
          {
            id : 3,
            msg : 'Cover Art'
          },
          {
            id : 4,
            msg : 'Contact Info'
          }
        ]
    }
  },
  components: {
    NavBar, 
    MainContent
  },
  methods : {
    change_page : function(msg) {
      if (typeof(msg) == "number" &  3 >= msg >= 0){
        this.activeID = msg;
      }
    }
  }
}



</script>

<style>
:root{
  --main-color: #282C34;
  --main-accent: #6FEB95;
  --secondary-accent: #4C8C65;
  --text-color: #FFFFFF;
}

@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300&display=swap');

#app {
  font-family: 'Quicksand', sans-serif;
  text-align: center;
  color: var(--text-color);
  margin: 0px;
  height: 100%;
  font-size: 30px;
}

a {
  color: #6feb95 !important;
}

a:visited {
  color: #0dc450 !important;
}

a:hover {
  color: #6feb95 !important;
}
</style>
