<template>
	<view class="container">
		
	
		<view>
			<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="2000">
				<swiper-item v-for="img in imgList" :key="img.id">
					<view class="swiper-item">
                        <navigator :url='"/pages/detail/detail?id=" + img.id' open-type="navigate">
                            {{img.content}}
                        </navigator>
					</view>
				</swiper-item>			
			</swiper>
		</view>
        <view class="intro">本项目已包含uni ui组件，无需import和注册，可直接使用。在代码区键入字母u，即可通过代码助手列出所有可用组件。光标置于组件名称处按F1，即可查看组件文档。</view>
        <text class="intro">详见：</text>
        <button type="default">{{btnName}}</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				href: 'https://uniapp.dcloud.io/component/README?id=uniui',
				btnName: 'btn',
				content: '我是内容',
                imgList: [{'content':'内容1', 'id':1}, {'content':'内容2', 'id':2}, {'content':'内容3', 'id':3}]
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
