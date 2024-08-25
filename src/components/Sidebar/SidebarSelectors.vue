<script setup lang="ts">
import Input from "@/components/shared/Input/Input.vue";
import Selector from "@/components/shared/Selector/Selector.vue";
</script>

<template>
  <div class="selectors">
    <Input />
    <Selector />
  </div>
</template>

<style lang="scss" scoped>
.selectors {
  display: flex;
  flex-direction: column;
  border-radius: 12px;
  background-color: rgba(255, 255, 255, 0.15);
  padding: 8px;
  margin-top: 24px;
  gap: 8px;
}
</style>
