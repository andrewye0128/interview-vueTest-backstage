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
    <h2
      class="text-center text-white h-[35px] leading-[35px] rounded-t-lg bg-blue-600 font-bold tracking-[3rem]"
    >
      紀錄
    </h2>
    <div class="bg-white px-1.5 pb-1.5">
      <table class="w-full text-sm text-left">
        <thead class="bg-blue-200">
          <tr class="text-center">
            <th class="text-blue-500 p-2">人臉辨識</th>
            <th class="text-blue-500 tracking-[1.2rem] p-2 pl-7">姓名</th>
            <th class="text-blue-500 p-2">進場時間</th>
            <th class="text-blue-500 p-2">出場時間</th>
            <th class="text-blue-500 p-2">滯留時間</th>
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
            <td class="flex justify-center items-center p-2">
              <img :src="person.avatar" class="size-12" />
            </td>
            <td class="p-2">{{ person.name }}</td>
            <td class="p-2">{{ person.entry }}</td>
            <td class="p-2">{{ person.exit }}</td>
            <td class="p-2">{{ person.duration }}</td>
            <td class="p-2">{{ person.card }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style scoped>
</style>
