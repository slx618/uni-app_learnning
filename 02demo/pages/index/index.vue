<template>
	<view class="content">
		<view style="background-color: #4CD964;color: #DD524D;width: 375rpx;">
			hello world
		</view>
		<view class="title">
			{{title}}
		</view>
		<!-- v-if 会删除 v-show 是隐藏 -->
		<view v-text="title" v-if="show" ></view>
		<!-- v-else  必须是相邻的 -->
		<view v-else> 你好</view>
		<view v-text="title" v-show="show" ></view>
		<view :class="c" v-html="title1" v-bind:style="style" v-on:click="click"></view>
		<button type="default" @click="content">点我</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello World',
				title1: '<p style="color:red">Hello World</p>',
				style: "font-size:50px",
				c:"bs",
				show: true
			}
		},
		onLoad() {
			console.log("load")
		},
		onShow() {
			console.log("show")
			
		},
		onHide() {
			console.log("hide")
		},
		methods: {
			click:function(){
				console.log('click')
				this.style = "font-size:60px"
				this.c = ""
			},
			content: function() {
				console.log('btnClick')
				this.show = !this.show
			}
		}
	}
</script>

<style>
	.title{
		background-color: #808080;
		font-size: 20px;
	}
	.bs {
		background-color: #007AFF;
	}
</style>
