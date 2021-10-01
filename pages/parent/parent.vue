<template>
	<view>
		<child @change='change' :text="text"></child>
		<chi-ld @change='change' :text="text"></chi-ld>
		{{childTitle}}
	</view>
</template>

<script>
	import child from '../../components/child.vue'
	import chiLd from '../../components/child.vue'
	export default {
		components:{
			child,
			chiLd
		},
		data() {
			return {
				text:'parent',
				childTitle: ''
			}
		},
		methods: {
			change(rst) {
				console.log(rst)
				this.childTitle = rst
			}
		},
		watch:{
			
		}
	}
</script>

<style>

</style>
