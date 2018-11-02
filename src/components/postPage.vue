<template>
	<div id="content">
		{{ content }}
	</div>
</template>

<script type="text/javascript">
	export default {
		name: 'postPage',
		data() {
			return {
				content: 'this is post page content'
			}
		}
	}
</script>

<style type="text/css">
	div {
		/*text-align: center;*/
		/*color: #eee;*/
	}
	#content {
		/*width: 30%;*/
		margin: auto;
		border: 2px solid #ccc;
	}
</style>