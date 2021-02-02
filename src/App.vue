<template>
  <div id="app">
   <!-- <Header></Header> -->
   <addblog />
  </div>
</template>

<script>
// import Header from './components/header.vue'
import Addblog from './components/addblog.vue'
export default {
  components:{
    // Header,
    Addblog
  }
}
</script>

<style>
html,body{
    padding: 0;
    margin: 0;
    height: 100%;
   
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

</style>
