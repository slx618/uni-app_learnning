<template>
	<view>
		 我是 child
		 <view class="">
		 	 父级来的变量 {{text}}
		 </view>
		 <button type="default" @click="click"> 子 button</button>
	</view>

</template>

<script>
	export default {
		props:{
			// text:Number
			text: [Number,String],
			default: "wewew"
		},
		data() {
			return {
				title: '我是子组件'
			};
		},
		methods:{
			click(){
				this.$emit('change', this.title)
			}
		}
	}
</script>

<style>

</style>
