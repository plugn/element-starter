<template>
	<div id="app">
		<img src="./assets/logo.png">
		<h1>{{ msg }}</h1>

		<el-button @click.native="startHacking">Yes!</el-button>

		<Tabs></Tabs>
	</div>
</template>

<script>
	import Tabs from './Tabs.vue'

	export default {
		components: {
			Tabs
		},
		data() {
			return {
				msg: 'Want something new?'
			}
		},

		methods: {
			startHacking() {
				this.$notify({
					title: 'Shhh',
					message: 'Just be patient...',
					duration: 6000
				})
			}
		}
	}
</script>

<style>
	#app {
		font-family: Helvetica, sans-serif;
		text-align: center;
	}
</style>
