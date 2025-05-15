<script setup>
import { Pie } from "vue-chartjs";
import { Chart as ChartJS, Title, Tooltip, Legend, ArcElement } from "chart.js";

// 註冊必要元件
ChartJS.register(Title, Tooltip, Legend, ArcElement);

// 定義圖表資料
const chartData = {
  labels: ["模板工", "木   工", "瓦   工", "泥水工", "檢測員"],
  datasets: [
    {
      label: '工種比例',
      backgroundColor: [
        "rgba(255, 24, 0, 0.8)", 
        "rgba(81, 162, 255, 1)", 
        "rgba(142, 197, 255, 1)", 
        "rgba(255, 223, 32, 1)", 
        "rgba(0, 201, 81, 1)"
      ],
      data: [5, 5, 3, 3, 1],
    },
  ],
}

// 圓餅圖設定
const chartOptions = {
  responsive: true,
  maintainAspectRatio: false,
  layout: {
    margin: {
      left: 150,
    },
    padding: {
      right: 50, // 增加右側內距，拉開 legend 與圖表距離
    },
  },
  plugins: {
    legend: {
      position: "right",
      align: "end",
      labels: {
        boxWidth: 20,
        padding: 15,
      },
    },
    title: {
      display: true,
      text: "",
    },
  },
};
</script>

<template>
  <Pie class="ml-[60px]" :data="chartData" :options="chartOptions" />
</template>

<style scoped></style>
