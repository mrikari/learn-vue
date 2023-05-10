<script setup lang="ts">
import Panel from '@/components/TrendPanel.vue.js'
</script>

<template>
  <div class="container m-auto grid gap-7 p-8">
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8">
      <Panel class="grid" :delta="6" iconColor="red" title="Title" />
      <Panel class="grid" :delta="-3" iconColor="blue" title="Title" />
      <Panel class="grid" :delta="9.5" iconColor="pink" title="Title" />
      <Panel class="grid" :delta="-12" iconColor="orange" title="Title" />
    </div>
  </div>
</template>

<style scoped></style>
