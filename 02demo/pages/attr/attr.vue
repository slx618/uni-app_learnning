<template>
	<view>
		{{fullText}}
		{{fullTextF()}}
 		<button type="default" @click="click"> 点我</button>
		{{name}}
	</view>
</template>

<script>
	export default {
		data() {
			return {
				first: 'hello',
				second: 'world',
				name: 'qq'
			}
		},
		methods: {
			click(){
				this.second = 'tt'
			},
			fullTextF(){
				console.log('fullTextF')
				return this.first + ' ' + this.second
			},
			
		},
		computed:{
			// 全绑定
			fullText(){
				// 计算属性涉及的变量变化的时候这个方法才会执行
				console.log('computed')
				return this.first + ' ' + this.second
			}
		},
		watch:{
			first(){
				console.log('watch first')
			},
			second(){
				console.log('watch second')
			}
		}
	}
</script>

<style>

</style>
