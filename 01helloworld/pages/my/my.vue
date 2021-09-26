<template>
	<view>
        <view class="page">
            {{c}}
        </view>
        <text>轮播图</text>
        <swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
            <swiper-item  v-for="img in imgList">
                <view class="swiper-item">
                    <text>{{img.txt}}</text>
                </view>
            </swiper-item>
         
        </swiper>
	</view>
    
</template>

<script>
	export default {
		data() {
			return {
				c:"这是我的内容",
                imgList: [
                    {txt:"xx1", id:"1"},
                    {txt:"xx2", id:"2"},
                ]
			}
		},  
        onLoad() {
            // uni.request({
            //     url:'',
            //     method:'POST',
            //     header:{
            //         'content-type': 'application/x-www-form-urlencode'
            //     },
            //     data:{
            //         qq:"x"
            //     },
            //     success: res => {
            //         console.log(res)
            //         this.imgList = res.data.data
            //     }
            // })
        },
		methods: {
			
		}
	}
</script>

<style>

</style>
