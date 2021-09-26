<template>
    <view>
       {{detail.id}}
    </view>
</template>

<script>
    export default {
        data() {
            return {
                detail: {
                   id: null
                }
            }
        },
        onLoad(params) {
            var id = params.id
            console.log("loding")
            console.log(id)
            this.detail.id = id
            // uni.request({
            //     url: "" + id,
            //     method: "POST",
            //     header:{},
            //     data: {},
            //     success: res => {
                    
            //     }
            // })
        },
        methods: {
            
        }
    }
</script>

<style>

</style>
