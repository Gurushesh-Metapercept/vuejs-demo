<template>
  <div id="app">
    <Navbar v-if="display"/>
    <img alt="Vue logo" src="./assets/logo.png">

    <Home v-if="display" data="Heleoooo" msg="hiii"/>

    <p class="homeStyle">{{ counter }}</p>

    <button v-on:click="counter = counter + 1">increase</button>


    <button v-on:click="toggle">toggle</button>

  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Home from './router/Home.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Home
  },

  data(){
    return {
      msg : "hellooooo",
      counter: 0,
      display : true
    }
  },
  methods: {
    toggle(){
        this.display =! this.display
      }
  },

  // beforeCreate will be called right after new Vue instance is initialized
  // data properties will be not accessible in this hook
  beforeCreate() {
    console.log("beforeCreate hook called")
  },

  // it gets called after beforeCreate Hook
  // in this hook we can access data properties 
  created() {
    console.log("created book called"+ " " + this.msg)
  },
  
  // beforeMount will be called after created() hook and right before Vue instance is mounted
  beforeMount(){
    console.log("beforeMount is called")
  },

  // mouted will be called after beforeMount hook and  vue instacne has been mounted
  // app component and other components become functional and ready to use.
  mounted(){
    console.log("mounted is called")
  },

  // beforeUpdate hook will be called after mounted hook
  // beforeUpdate is called any time a change is made to the data that requires the DOM to be updated.

  // When we change data() or cause a re-render in our component, an update event will fire. 
  // Immediately before the re-render occurs, beforeUpdate() hook will fire. 
  beforeUpdate(){
    console.log("beforeUpdate is called", this.counter)
  },


  // updated hook will be called after the beforeUdated hook and just after DOM update occurred.
  updated(){
    console.log("updated hook is called", this.counter)
  },

  

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
.homeStyle{
    color: rgb(196, 134, 2);
  }
</style>
