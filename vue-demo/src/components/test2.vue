<template>
    <h3>生命周期函数</h3>
    <p>{{ message }}</p>
    <button @click="message = 'Hello Vue!'">更新消息</button>
</template>

<script lang="ts">
    export default {
        data() {
            return {
                message:''
            }
    },
    beforeCreate() {
            console.log("beforeCreate:组件创建之前");
    },
    created() {
            console.log("created:组件创建完成");
    },
    beforeMount() {
            console.log("beforeMount:挂载之前");
    },
    mounted() {
        console.log("mounted:挂载完成")
    },
    beforeUpdate() {
        console.log("beforeUpdate:更新之前")
    },
    updated() {
        console.log("updated:更新完成")
    },
    beforeUnmount() {
        console.log("beforeUnmount:销毁之前")
    },
    unmounted() {
        console.log("unmounted:销毁完成")
    },
    }
</script>