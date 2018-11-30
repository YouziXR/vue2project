<template>
  <div id="root">
    <h3>
    {{ articles.title }}
  </h3>
    <h4>
    {{ articles.author.firstAuthor }}
    <!-- {{ obj.nothing }} -->
  </h4>
    <h5>
    {{ articles.body }}
  </h5>
    <input type="button" name="focus_btn" v-focus>
  </div>
</template>
<script type="text/javascript">
export default {
  name: 'homeContent',
  // props: ['title', 'body', 'author', 'obj'],
  props: {
    // obj: Object,
    articles: Object
  },
  directives: {
    focus: {
      inserted: function(el) {
        el.focus();
      }

    }
  }
}

</script>
<style type="text/css">
</style>
