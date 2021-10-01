<template>
	<view>
		<button type="default" @click="click">flash</button>
		<view class="" >
			{{text}}
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				text:'hello'
			}
		},
		methods: {
			click(){
				this.text = 'world'
			}
		},
		beforeCreate() {
			console.log('beforeCreate: ' + this.text)
		},
		created() {
			console.log('create: ' + this.text)
		},
		beforeMount() {
			console.log('beformMount')
		},
		mounted() {
			console.log('mounted')
		},
		
		 // 页面更新才会触发
		beforeUpdate() {
			console.log('beforeUpdate')
		},
		updated() {
			console.log('update')
		}
	}
</script>

<style>

</style>
