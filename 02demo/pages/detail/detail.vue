<template>
	<view>
		<input type="text" value="" v-model="text"/>
		<button type="default" @click="click"> 提交</button>
		 <view class="">
			<view class="" v-for="v in list">
				{{v}}
			</view>
		 </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				text: null,
				list:['hello', 'world']
			}
		},
		methods: {
			click() {
				console.log(this.text)
				this.list.push(this.text)
				this.text = ''
				
			}
		}
	}
</script>

<style>

</style>
