<script setup>
import ArrowIcon from "./icons/IconArrow.vue";

const menu = [
  { label: "儀錶板", icon: "fa-solid fa-gauge-simple-high" },
  { label: "看板管理", icon: "fa-solid fa-chalkboard" },
  {
    label: "資料管理",
    icon: "fa-solid fa-folder",
    children: [
      "人員管理",
      "車輛管理",
      "日誌管理",
      "出勤管理",
      "門禁管理",
      "派車管理",
      "費用管理",
    ],
  },
  { label: "推送管理", icon: "fa-solid fa-share-nodes" },
  { label: "權限管理", icon: "fa-solid fa-lock" },
];
</script>

<template>
  <!-- Sidebar -->
  <aside class="fixed top-0 bottom-0 w-64 bg-blue-100 p-4 text-sm">
    <div class="w-[80%] mx-auto">
      <img
        class="bg-blue-100 mb-8"
        src="https://github.com/weijanlin/frontend/blob/main/microsys_logob290x6001.jpg?raw=true"
        alt="MICROSYS 圖片"
      />
      <nav>
        <ul>
          <li v-for="(item, index) in menu" :key="index" class="mb-2 group cursor-pointer">
            <div class="flex items-center justify-between px-2 py-1 rounded">
              <div
                class="flex items-center space-x-2 text-blue-900 cursor-pointer group-hover:text-blue-600"
              >
                <span><i :class="item.icon"></i></span>
                <span>{{ item.label }}</span>
              </div>
              <ArrowIcon class="size-[15px] group-hover:text-blue-600" />
            </div>

            <!-- 子選單 -->
            <ul v-if="item.children" class="ml-6 mt-3 space-y-1">
              <li
                v-for="(child, cIdx) in item.children"
                :key="cIdx"
                class="flex justify-between items-center w-[148px] text-sm mb-4 text-blue-800 cursor-pointer hover:text-blue-600"
              >
                • {{ child }}
                <ArrowIcon class="size-[12px]" />
              </li>
            </ul>
          </li>
        </ul>
      </nav>
    </div>
  </aside>
</template>
<style scoped></style>
