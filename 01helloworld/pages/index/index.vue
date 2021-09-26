<template>
	<view class="container">
		
		<view class="intro">本项目已包含uni ui组件，无需import和注册，可直接使用。在代码区键入字母u，即可通过代码助手列出所有可用组件。光标置于组件名称处按F1，即可查看组件文档。</view>
		<text class="intro">详见：</text>
		<uni-link :href="href" :text="href"></uni-link>
		<button type="default">{{btnName}}</button>
		<view>
			<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="2000">
				<swiper-item>
					<view class="swiper-item">
						 内容 1
					</view>
				</swiper-item>
				<swiper-item>
					<view class="swiper-item">
						内容 2
					</view>
				</swiper-item>
                <swiper-item>
                	<view class="swiper-item">
                		内容 3
                	</view>
                </swiper-item>
			</swiper>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				href: 'https://uniapp.dcloud.io/component/README?id=uniui',
				btnName: 'btn',
				content: '我是内容',
			}
		},
		methods: {

		}
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
</style>
