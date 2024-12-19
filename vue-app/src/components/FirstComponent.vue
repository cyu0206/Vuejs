<template>
    <h2 id="myH">第一個 component</h2>
</template>

<style scoped>
    h2{
        color:blue;
        background-color: aquamarine;
    }
</style>
<script setup>
import { onMounted } from 'vue';
    onMounted(()=>{
        const theH = document.querySelector('#myH');
        console.log(theH);
        console.log(theH.textContent);
    })


</script>