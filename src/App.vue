<template>
  <div id="app">
    <img src="./assets/logo.png">
    <!-- <router-view/> -->
    <myApp></myApp>
    <hello-world></hello-world>
    <pages></pages>
  </div>
</template>
<script>
import HelloWorld from './components/HelloWorld'
import myApp from './myApp'
import pages from './components/pages'
export default {
  name: 'App',
  components: {
    HelloWorld,
    myApp,
    pages
  },
  data() {
    return {

    }
  },
  methods: {

  },
  computed: {

  }
}

</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
  /*display: flex;*/
  /*margin: auto;*/
}

</style>
