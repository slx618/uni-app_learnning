<template>
    <view>
        <image src="../../static/logo.png" mode="aspectFill"></image>
    </view>
</template>

<script>
    export default {
        data() {
            return {
                
            }
        },
        methods: {
            
        },
        mounted() {
            uni.chooseImage({
                count: 6, //默认9
                sizeType: ['original', 'compressed'], //可以指定是原图还是压缩图，默认二者都有
                success: function (res) {
                    console.log(JSON.stringify(res.tempFilePaths));
                }
            });
        }
    }
</script>

<style>

</style>
