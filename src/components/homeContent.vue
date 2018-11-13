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
  </div>
</template>
<script type="text/javascript">
export default {
  name: 'homeContent',
  // props: ['title', 'body', 'author', 'obj'],
  props: {
  	// obj: Object,
  	articles: Object
  }
}

</script>
<style type="text/css">
	
</style>

