<script setup>
const cards = [
  {
    id: 1,
    bgcolor: "bg-blue-400",
    icon: "text-2xl fa-solid fa-user",
    words: ["今日人容數"],
    number: 0,
  },
  {
    id: 2,
    bgcolor: "bg-yellow-300",
    icon: "text-3xl fa-solid fa-triangle-exclamation",
    iconsize: "text-3xl",
    words: ["今日累計", "未戴安全帽次數"],
    number: 0,
  },
  {
    id: 3,
    bgcolor: "bg-yellow-300",
    icon: "text-3xl fa-solid fa-triangle-exclamation",
    words: ["今日累計", "危險區域警報次數"],
    number: 0,
  },
  {
    id: 4,
    bgcolor: "bg-green-500",
    icon: "text-3xl fa-solid fa-triangle-exclamation",
    words: ["本週累計", "未戴安全帽次數"],
    number: 0,
  },
  {
    id: 5,
    bgcolor: "bg-green-500",
    icon: "text-3xl fa-solid fa-triangle-exclamation",
    words: ["本週累計", "危險區域警報次數"],
    number: 0,
  },
];

</script>

<template>
  <div class="grid grid-cols-5 gap-4 mb-4 text-white text-center text-sm">
    <div
      v-for="card in cards"
      :key="card.id"
      :class="card.bgcolor"
      class="flex justify-between items-center rounded-xl p-3"
    >
      <div class="flex gap-2 justify-center items-center">
        <i :class="card.icon"> </i>
        <div>
          <p v-for="(word, index) in card.words" :key="index" class="text-left">
            {{ word }}
          </p>
        </div>
      </div>
      <p class="text-4xl">{{ card.number }}</p>
    </div>
  </div>
</template>

<style></style>
