<script setup>
import { RouterLink, RouterView } from "vue-router";
import SideBar from "./components/SideBar.vue";
import HeaderAdmin from "./components/HeaderAdmin.vue";

</script>

<template>
  <div class="flex flex-row">

    <!-- Sidebar -->
    <SideBar />

    <!-- 取代SideBar 佔據其空間 basis-64 -->
    <div class="basis-64"></div>

    <div class="grow">
      <!-- header -->
      <HeaderAdmin />
      <RouterView />
    </div>
  </div>
</template>

<style scoped>
</style>
