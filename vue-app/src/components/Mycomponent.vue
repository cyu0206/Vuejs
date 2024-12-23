<!-- <script>
    export default{
        data() {
        return {message:"Options API"}
        }
    }
</script> -->

<script setup>
import { ref } from 'vue';
    const message = ref("setup 語法糖")
    const count =ref(0)

    const add =()=>{
        count.value++
    }
    
</script>

<template>
    <div>
        <input type="text" v-model="message" />
        <h2>第二個 Component {{ message }}</h2>
        <h2 style="color:green">建立的第一個組件</h2>
        <h2  style="color:blue">這是第二個組件</h2>
        <button @click="add">{{ count }}</button>
    </div>
</template>

<style scoped>
    /* h2 {
        color:blue
    }
    h3 {
        color:green
    } */
</style>