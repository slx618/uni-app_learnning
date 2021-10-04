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
            }
        }
    }
</script>

<style>

</style>
