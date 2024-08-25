<script setup lang="ts">
import Button from "@/components/shared/Button/Button.vue";
</script>

<template>
  <div class="sidebar-header">
    <Button class="action-btn" type="hover">Edit</Button>
    <span class="counter">7 items</span>
    <Button class="action-btn" type="hover">New</Button>
  </div>
</template>

<style scoped>
.sidebar-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

.action-btn {
  min-height: 46px;
}

.counter {
  font-size: 0.75rem;
  line-height: 1rem;
  color: rgba(0, 0, 0, 0.4);
  cursor: default;
  font-weight: 600;
}
</style>
