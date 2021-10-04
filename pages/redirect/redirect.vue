<template>
    <view>
        <navigator url="../index/index" open-type="switchTab">
            <button type="default">跳转</button>
        </navigator>
        <button type="default" @click="click">api 跳转</button>
        <button type="default" @click="click1">api 跳转 redirect</button>
    </view>
</template>

<script>
    export default {
        data() {
            return {
                
            }
        },
        methods: {
            click(){
                uni.switchTab({
                    url:"../index/index",
                    
                })
            },
            click1(){
                uni.redirectTo({
                    url: "../request/request"
                })
            }
        },
        onUnload() {
            console.log('页面关')
        }
    }
</script>

<style>

</style>
