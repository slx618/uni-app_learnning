<template>
    <view>
        <button type="default" @click="click">打印</button>
    </view>
</template>

<script>
    export default {
        data() {
            return {
                text:'hello'
            }
        },
        methods: {
            click() {
                var t = setTimeout(() => {
                    console.log('log:'+ this.text)
                }, 2000)
                var it = setInterval(() => {
                    console.log('setInterval:' + this.text)
                }, 3000)
            }
        }
    }
</script>

<style>

</style>
