<template>
  <div class="grid grid-cols-2 gap-4 mb-4">
    <!-- Bar Chart-->
    <div class="bg-white shadow rounded">
      <h2
        class="text-center text-white h-[35px] leading-[35px] rounded-t-lg bg-blue-600 font-bold"
      >
        場域人員統計（長條圖）
      </h2>
      <div class="w-[65%] h-[250px] mx-auto">
        <BarChart />
      </div>
    </div>

    <!-- Pie Chart -->
    <div class="bg-white shadow rounded">
      <h2
        class="text-center text-white h-[35px] leading-[35px] rounded-t-lg bg-blue-600 font-bold"
      >
        場域人員統計（圓餅圖）
      </h2>
      <div class="w-[80%] h-[235px] max-w-[700px] mx-auto">
        <PieChart />
      </div>
    </div>
  </div>
</template>
<script setup>
import  BarChart from "./charts/BarChart.vue";
import  PieChart from "./charts/PieChart.vue";

</script>
<style scoped></style>
