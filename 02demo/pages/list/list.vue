<template>
	<view>
		<view class="" v-for="item, index in 10" :key="index">
			{{index}} hello world {{item}}
		</view>
		<view class="" v-for="item,k in list">
			{{k}} hello world! {{item}}
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: [
					'he', 'she'
				]
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
