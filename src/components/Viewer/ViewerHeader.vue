<script setup lang="ts">
import ProgressIcon from "@/icons/ProgressIcon.vue";
import CheckIcon from "@/icons/CheckIcon.vue";
import MinusIcon from "@/icons/MinusIcon.vue";
import Button from "@/components/shared/Button/Button.vue";
</script>

<template>
  <header class="header">
    <div class="options">
      <Button type="hover" title="Progress Wheel">
        <ProgressIcon />
      </Button>
      <Button type="hover" title="Mark as Completed">
        <CheckIcon />
      </Button>
    </div>
    <span class="date">21.11.22 at 13:41</span>
    <Button type="hover" title="Remove Note">
      <MinusIcon />
    </Button>
  </header>
</template>

<style scoped lang="scss">
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
}

.options {
  display: flex;
  gap: 5px;
  align-items: center;
}

.date {
  font-size: 0.75rem; /* 12px */
  line-height: 1rem; /* 16px */
  color: rgba(0, 0, 0, 0.4);
  font-weight: 600;
}
</style>
