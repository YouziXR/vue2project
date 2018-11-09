<template>
	<div id="content">
		{{ content }}
		
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
				content: 'this is home page content'
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