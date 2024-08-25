<script setup lang="ts"></script>

<template>
  <div class="selector">
    <div class="option active">All</div>
    <div class="divider" />
    <div class="option">Done</div>
    <div class="divider" />
    <div class="option">Undone</div>
    <div class="divider" />
    <div class="option">In progress</div>
  </div>
</template>

<style scoped lang="scss">
.selector {
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-radius: 8px;
  background-color: rgba(255, 255, 255, 0.3);
}

.option {
  min-height: 32px;
  display: flex;
  align-items: center;
  border-radius: 8px;
  padding: 0 18px;
  color: #000;
  font-weight: 600;
  cursor: pointer;
}

.active {
  color: #fff;
  background-color: #000;
}

.divider {
  height: 10px;
  width: 2px;
  border-radius: 8px;
  background-color: rgba(0, 0, 0, 0.2);
}
</style>
