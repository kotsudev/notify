<script setup lang="ts">
import SidebarHeader from "@/components/Sidebar/SidebarHeader.vue";
</script>

<template>
  <div class="sidebar">
    <SidebarHeader />
  </div>
</template>

<style lang="scss" scoped>
.sidebar {
  display: flex;
  flex-direction: column;
  padding: 24px;
}
</style>
