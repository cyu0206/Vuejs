<script setup>
    import { ref, computed } from 'vue';

    const height = ref(0); // 身高 (公分)
    const weight = ref(0); // 體重 (公斤)

    const bmi = computed(() => {
    if (height.value <= 0 || weight.value <= 0) {
        return '請輸入有效數值'; // 處理輸入無效的情況
    }

    const heightInMeters = height.value / 100; // 將公分轉換成公尺
    const bmiValue = weight.value / (heightInMeters * heightInMeters);
        return bmiValue.toFixed(2); // 計算 BMI 並保留兩位小數
    });
    const celsius = ref(0)
</script>

<template>
    <div>
        <h2>Computed Demo</h2>
    </div>
    <div>
        攝氏度:<input type="text" v-model="celsius">
    </div>
    <div>
        華氏：{{ (celsius * 9 / 5) + 32 }}
    </div>

    <div>
    <h2>BMI</h2>
  </div>
  <div>
    身高 (公分): <input type="number" v-model.number="height">
  </div>
  <div>
    體重 (公斤): <input type="number" v-model.number="weight">
  </div>
  <div>
    BMI：{{ bmi }}
  </div>
    <div v-if="bmi !== '請輸入有效數值'">
        <p v-if="bmi < 18.5">體重過輕</p>
        <p v-else-if="bmi < 24">正常範圍</p>
        <p v-else-if="bmi < 27">過重</p>
        <p v-else-if="bmi < 30">輕度肥胖</p>
        <p v-else-if="bmi < 35">中度肥胖</p>
        <p v-else>重度肥胖</p>
    </div>
</template>

<style lang="css" scoped>

</style>