<template>
  <div id="app">
    <img src="./assets/logo.png">
    <!-- <router-view/> -->
    <myApp></myApp>
    <HelloWorld></HelloWorld>
    <div id="navbar">
      <button v-for="page in pages" :key="page" @click="changePage(page)" class="page-button">
        {{ page }}
      </button>
    </div>
    <component :is="currentPageComponent" class="page-content">
    </component>
  </div>
</template>
<script>
import HelloWorld from './components/HelloWorld'
import myApp from './myApp'
import homePage from './components/homePage'
import postPage from './components/postPage'
import archivePage from './components/archivePage'
export default {
  name: 'App',
  components: {
    HelloWorld,
    myApp,
    homePage,
    postPage,
    archivePage
  },
  data() {
    return {
      currentPage: 'homePage',
      pages: ['homePage', 'postPage', 'archivePage']
    }
  },
  methods: {
    changePage: function(page) {
      this.currentPage = page;
    }
  },
  computed: {
    currentPageComponent: function() {
      return this.currentPage;
    }
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
#navbar  {
  /*margin-left: 0;*/
  margin: auto;
  width: 30%;
  /*border: 2px solid #ccc;*/
  text-align: left;
}
.page-button {
  /*margin-left: 0;*/
  border: 1px solid #ccc;
  background: #f0f0f0;
  border-radius: 3px 3px 0 0;
  box-shadow: 0px 0px;
  padding: 6px 10px
}
.page-content {
  text-align: left;
  margin: auto;
  width: 30%;
  border: 1px solid #ccc;
}
</style>
