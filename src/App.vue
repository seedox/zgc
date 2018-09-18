<template>
  <div id="app">
    <TopBar/> 
    <div class="container">
      <Aside/>
      <Main/>
    </div>  
  </div>
</template>

<script>
import TopBar from './components/TopBar.vue'
import Aside from './components/Aside.vue'
import Main from './components/Main.vue'

export default {
  name: 'app',
  components: {
    TopBar,
    Aside,
    Main
  }
}
</script>

<style>
html,body{
  height:100%;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  height:100%; 
  display: flex;
  flex-direction: column;
  user-select:none;
}
.container{
  display:flex;
  flex:1;
}
</style>
