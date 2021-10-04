<template>
    <view class="page">
	   <view class="player">
		   <video :poster="detail.poster" :src="detail.vUrl" controls="true"></video>
	   </view>
    </view>
</template>

<script>
    export default {
        props:{
        	// text:Number
        	id: [Number,String],
        	default: "wewew"
        },
        data() {
           
            return {
                detail: {
				   vUrl: "",
				   poster: ""
				   
                }
            }
        },
        onLoad(params) {
            var id = params.id
            console.log("detail + params.id")
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
