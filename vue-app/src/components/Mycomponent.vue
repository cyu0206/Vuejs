<script>
    export default{
        data() {
        return {message:"Options API"}
        }
    }
</script>

<template>
    <div>
        <input type="text" v-model="message" />
        <h2 style="color:green">建立的第一個組件</h2>
        <h2  style="color:blue">這是第二個組件</h2>
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