<template>
    <div class="test1">
        <h1>你好呀</h1>
        <h3>学习3.0</h3>
        <h1>{{ title }}</h1>
        <h1>age = {{ age }}</h1>
        <ul>
            <li v-for="(name,index) in names" :key = "index">{{ name }}</li>
        </ul>
    </div>
</template>

<script lang="ts">
export default {
    name: "test1",
    props: {
        title: {
            type: String,
            default: ""
        },
        age: {
            type: Number,
            default: 0
        },
        names: {
            type: Array,
            default: () => []
        }
    },
    data() {
        return {
            
        }
    }
}
</script>

<style scoped>
h3{
    color: red;
}
</style>