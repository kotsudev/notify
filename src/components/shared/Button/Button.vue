<script setup lang="ts">
import { computed } from "vue";
type ButtonType = "inline" | "primary" | "hover";

interface Props {
  type?: ButtonType;
}

const props = withDefaults(defineProps<Props>(), {
  type: "inline",
});

const btnClass = computed(() => ({
  [props.type]: true,
  btn: true,
}));
</script>

<template>
  <button :class="btnClass">
    <slot></slot>
  </button>
</template>

<style lang="scss" scoped>
.btn {
  height: 100%;
  display: flex;
  align-items: center;
  border-radius: 8px;
  border: 1px solid transparent;
  padding: 0.5em 1em;
  font-size: 16px;
  font-family: inherit;
  cursor: pointer;
  background-color: transparent;
  color: #000;
  font-weight: 700;
}

.inline {
  padding: 0.2em;
  &:hover {
    border-color: transparent;
    background-color: transparent;
  }
}

.hover {
  padding: 6px;

  &:hover {
    background-color: rgba(255, 255, 255, 0.15);
  }
}
</style>
