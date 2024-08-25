<script setup lang="ts">
import Button from "@/components/shared/Button/Button.vue";
</script>

<template>
  <div class="sidebar-header">
    <Button>Edit</Button>
    <span class="counter">7 items</span>
    <Button>New</Button>
  </div>
</template>

<style scoped>
.sidebar-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

.counter {
  color: #000;
  font-size: 14px;
  cursor: default;
}
</style>
