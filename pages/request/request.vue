<template>
    <view>
        <button type="default" @click="getInfo()">点我</button>
        <view v-for="v in data" :key="v.id">
            <view>{{v.name}}</view>
        </view>
    </view>
</template>

<script>
    export default {
        data() {
            return {
                data: null
            }
        },
        methods: {
            getInfo() {
                uni.request({
                    url: "http://localhost/content.json",
                    dataType: "json",
                    success(res) {
                        this.data = res.data.list
                        console.log(this.data)
                    }
                })
            }
        },
        mounted() {
             this.getInfo()
        }
      
    }
</script>

<style>

</style>
