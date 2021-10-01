<template>
    <view class="page">
	   <view class="player">
		   <video :poster="detail.poster" :src="detail.vUrl" controls="true"></video>
	   </view>
    </view>
</template>

<script>
    export default {
        data() {
            return {
                detail: {
                   id: null,
				   vUrl: "",
				   poster: ""
				   
                }
            }
        },
        onLoad(params) {
            var id = params.id
            console.log("loding")
            console.log(id)
            this.detail.id = id
      //       uni.request({
      //           url: "" + id,
      //           method: "POST",
      //           header:{},
      //           data: {},
      //           success: rst => {
						// this.detail = rst.data.data
      //           }
      //       })
        },
        methods: {
            
        }
    }
</script>

<style>

</style>
