<template>
    <view>
        
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
        created() {
            uni.setStorage({
                key: 'storage_key',
                data: 'hello',
                success: function () {
                    console.log('success');
                }
            });
            uni.setStorageSync('storage_key', 'hello');
            uni.getStorage({
                key:'storage_key',
                success(rst) {
                    console.log(rst)
                }
            });
            var rst = uni.getStorageSync('storage_key')
            console.log(rst)
        }
    }
</script>

<style>

</style>
