<script setup lang="ts">
import SidebarAgenda from '@/components/SidebarAgenda.vue'
</script>

<template>
  <div class="layout">
    <SidebarAgenda />
    <main></main>
  </div>
</template>

<style scoped>
.layout {
  display: flex;
  align-items: flex-start;
  gap: 24px;
  flex: 1 0 0;
  align-self: stretch;
}

.main {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 32px;
  flex: 1 0 0;
  align-self: stretch;
}
</style>
