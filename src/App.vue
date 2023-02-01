<template>
  <div id="app">
    <Navbar/>
    <img alt="Vue logo" src="./assets/logo.png">
    <Home data="Heleoooo" msg="hiii"/>

  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Home from './components/Home.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Home
  }
}
</script>

<style>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
