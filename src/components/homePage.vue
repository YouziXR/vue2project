<template>
	<div id="content">
		<!-- {{ content }} -->
		<homeContent v-bind:articles="articles"></homeContent>

	</div>
</template>

<script type="text/javascript">

	import homeContent from './homeContent'

	export default {
		name: 'homePage',
		components: {
			homeContent
		},
		data() {
			return {
				content: 'this is home page content',
				articles: {
					title: 'first title',
					body: 'first body',
					author: {
						firstAuthor: 'Steve',
						secondAuthor: 'Steven'
					}
				},
				/*obj: {
					nothing: 'nothing'
				}*/
			}
		}
	}
</script>

<style type="text/css">
	div {
		/*text-align: center;*/
		/*color: #eee;*/
	}
</style>