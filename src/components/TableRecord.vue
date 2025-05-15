<script setup>

const people = [
  {
    name: "丁小雨",
    bgcolor: "bg-white",
    avatar: "https://i.pravatar.cc/40?img=1",
    entry: "2025/03/19 19:10",
    exit: "2025/03/19 19:10",
    duration: "00:30:00",
    card: "115030218",
  },
  {
    name: "王大成",
    bgcolor: "bg-blue-100",
    avatar: "https://i.pravatar.cc/40?img=2",
    entry: "2025/03/19 19:10",
    exit: "2025/03/19 19:10",
    duration: "00:30:00",
    card: "115030218",
  },
  {
    name: "不明人士",
    bgcolor: "bg-red-100",
    avatar: "https://i.pravatar.cc/40?img=3",
    entry: "2025/03/19 19:10",
    exit: "2025/03/19 19:10",
    duration: "00:30:00",
    card: "115030218",
  },
];
</script>

<template>
  <!-- Table  -->
  <div class="bg-white rounded-xl shadow overflow-auto">
    <p
      class="text-center text-white h-[25px] leading-[25px] rounded-t-lg bg-blue-600 font-bold tracking-[3rem]"
    >
      紀錄
  </p>
    <div class="bg-white px-1">
      <table class="w-full text-sm text-left">
        <thead class="bg-blue-200">
          <tr class="text-center">
            <th class="text-blue-500 p-2 border-r-3 border-white">人臉辨識</th>
            <th class="text-blue-500 tracking-[1.2rem] p-2 pl-7 border-r-3 border-white">姓名</th>
            <th class="text-blue-500 p-2 border-r-3 border-white">進場時間</th>
            <th class="text-blue-500 p-2 border-r-3 border-white">出場時間</th>
            <th class="text-blue-500 p-2 border-r-3 border-white">滯留時間</th>
            <th class="text-blue-500 p-2">聯安卡</th>
          </tr>
        </thead>
        <tbody>
          <tr
            v-for="person in people"
            :key="person.name"
            :class="person.bgcolor"
            class="text-center"
          >
            <td class="flex justify-center items-center pt-1">
              <img :src="person.avatar" class="size-12" />
            </td>
            <td>{{ person.name }}</td>
            <td>{{ person.entry }}</td>
            <td>{{ person.exit }}</td>
            <td>{{ person.duration }}</td>
            <td>{{ person.card }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style scoped>
</style>
