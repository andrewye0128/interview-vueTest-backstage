<script setup>
import TableRecord from "../components/TableRecord.vue";
import ChartPanel from "../components/ChartPanel.vue";
import CardAdmin from "../components/CardAdmin.vue";
import FooterAdmin from "../components/FooterAdmin.vue";

// const openReadmeInEditor = () => fetch("/__open-in-editor?file=README.md");

</script>

<template>
  <main class=" bg-sky-100/50 px-4 pt-10">

    <!-- Cards -->
    <CardAdmin />

    <!-- Charts -->
    <ChartPanel />

    <!-- Table  -->
    <TableRecord />

    <!-- footer -->
    <FooterAdmin />
  </main>
</template>
