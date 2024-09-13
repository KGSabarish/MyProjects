<template>
  <img alt="Vue logo" src="./assets/logo.png">
   <!-- <p>{{ sample }}</p> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  <!-- <HelloWorld @my-event="myAction" />
  <HelloWorld :is="currentComponent" /> -->
  <component v-if= "sample < 0" :is="currentComponent"></component>
  <HelloWorld msg="Welcome to Your Vue.js App" />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
//import Test from './components/Test.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
  },
  data() {
    return {
      sample: 1,
      currentComponent: 'App'
    }
  },
  methods: {
    myAction(name) {
      alert("Emit function should work with Name: ", name)
    }
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
  margin-top: 60px;
}
</style>
