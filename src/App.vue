<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header class="flex justify-center h-16 bg-black shadow-sm">
    <div class="container flex flex-row items-center justify-between">
      <RouterLink to="/">
        <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="25" height="25" />
      </RouterLink>
      <nav>
        <div class="flex flex-row items-center gap-6">
          <RouterLink to="/" class="text-white">Dashboard</RouterLink>
          <RouterLink to="/about" class="text-white">About</RouterLink>
        </div>
      </nav>
    </div>
  </header>
  <RouterView />
</template>

<style scoped></style>
