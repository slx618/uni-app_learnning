<template>
	<view>
        <view class="page">
            {{c}}
        </view>
	</view>
    
</template>

<script>
	export default {
		data() {
			return {
				c:"这是我的内容"
               
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
            //     success: rst => {
            //         console.log(rst)
            //         this.imgList = rst.data.data
            //     }
            // })
        },
		methods: {
			
		}
	}
</script>

<style>

</style>
