<script setup>
import { ref, computed } from "vue";
import { Bar } from "vue-chartjs";
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  BarElement,
  CategoryScale,
  LinearScale,
} from "chart.js";

ChartJS.register(
  Title,
  Tooltip,
  Legend,
  BarElement,
  CategoryScale,
  LinearScale
);

// 定義圖表資料
const labels = ["模板工", "木工", "瓦工", "泥水工", "檢測員"]; // X 軸有六個分類

const chartData = {
  labels,
  datasets: [
    {
      label: "模板工",
      data: [5],
      backgroundColor: "rgba(255, 24, 0, 0.8)",
      barThickness: 30,
    },
    {
      label: "木   工",
      data: [0, 5],
      backgroundColor: "rgba(81, 162, 255, 1)",
      barThickness: 30,
    },
    {
      label: "瓦   工",
      data: [0, 0, 3],
      backgroundColor: "rgba(142, 197, 255, 1)",
      barThickness: 30,
    },
    {
      label: "泥水工",
      data: [0, 0, 0, 3],
      backgroundColor: "rgba(255, 223, 32, 1)",
      barThickness: 30,
    },
    {
      label: "檢測員",
      data: [0, 0, 0, 0, 1],
      backgroundColor: "rgba(0, 201, 81, 1)",
      barThickness: 30,
    },
  ],
};

const chartOptions = {
  responsive: true,
  maintainAspectRatio: false,
  // layout: {
  //   padding: {
  //     left: 120, // 增加右側內距，拉開 legend 與圖表距離
  //   },
  // },
  plugins: {
    legend: {
      position: "right",
      align: "end",
      labels: {
        padding: 20, // 每個 legend 項目之間的間距
        boxWidth: 20,
      },
    },
    title: {
      display: true,
      text: "",
    },
  },
  scales: {
    x: {
      stacked: true, // 讓它們堆疊在同一根柱子上
      grid: {
        display: false, // 移除 x 軸網格
      },
    },
    y: {
      beginAtZero: true,
      ticks: {
        stepSize: 1,
      },
      grid: {
        display: false, // 移除 y 軸網格
      },
    },
  },
};
</script>

<template>
  <Bar :data="chartData" :options="chartOptions" />
</template>
<style scoped></style>
