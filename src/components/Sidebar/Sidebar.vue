<script setup lang="ts">
import SidebarHeader from "@/components/Sidebar/SidebarHeader.vue";
import SidebarSelectors from "@/components/Sidebar/SidebarSelectors.vue";
import Note from "@/components/Note/Note.vue";
</script>

<template>
  <SidebarHeader />
  <SidebarSelectors />
  <span class="date">Today</span>
  <div class="scroll-wrapper">
    <div class="notes">
      <Note />
      <div class="divider" />
      <Note />
      <div class="divider" />
      <Note />
      <div class="divider" />
      <Note />
      <div class="divider" />
      <Note />
      <div class="divider" />
      <Note />
      <div class="divider" />
      <Note />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.date {
  color: rgba(0, 0, 0, 0.4);
  font-size: 12px;
  font-weight: 300;
  text-align: center;
  margin: 9px 0 9px;
}

.divider {
  width: 100%;
  height: 1px;
  background-color: rgba(0, 0, 0, 0.15);
  border-radius: 8px;
}

.scroll-wrapper {
  overflow: scroll;
  border-radius: 8px;
}

.notes {
  display: flex;
  flex-direction: column;
  gap: 8px;
}
</style>
