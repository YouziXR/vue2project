<template>
  <div id="pages">
    <div id="navbar">
      <button v-for="page in pages" :key="page" @click="changePage(page)" :class="['page-button', { active: currentPage === page }]">
        {{ page }}
      </button>
    </div>
    <component :is="currentPageComponent" class="page-content">
    </component>
  </div>
</template>
<script type="text/javascript">
import homePage from './homePage'
import postPage from './postPage'
import archivePage from './archivePage'

export default {
  name: 'pages',
  components: {
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
<style type="text/css">
#navbar {
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
  /*box-shadow: 0px 0px;*/
  margin-left: -1px;
  padding: 6px 10px;
}

.page-button.active {
  background: #e0e0e0;
}

.page-button:hover {
  background: #e0e0e0;
}

.page-content {
  text-align: left;
  margin: auto;
  width: 30%;
  border: 1px solid #ccc;
}

</style>
