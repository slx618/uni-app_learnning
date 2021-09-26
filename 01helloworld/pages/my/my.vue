<template>
	<view>
        <view class="page">
            {{c}}
        </view>
        <text>xxxx</text>
        <swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
            <swiper-item>
                <view class="swiper-item">
                    <text>mytext1</text>
                </view>
            </swiper-item>
            <swiper-item>
                <view class="swiper-item">
                    <text>mytext2</text>
                    
                </view>
            </swiper-item>
        </swiper>
	</view>
    
</template>

<script>
	export default {
		data() {
			return {
				c:"这是我的内容"
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
