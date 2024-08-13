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
  border-radius: 8px;
  border: 1px solid transparent;
  padding: 0.5em 1em;
  font-size: 16px;
  font-family: inherit;
  cursor: pointer;
  background-color: transparent;
  color: #000;

  &:hover {
    border-color: transparent;
    background-color: rgba(255, 255, 255, 0.15);
  }

  &:focus,
  &:focus-visible {
    outline: thin solid rgba(255, 255, 255, 0.15);
  }
}

.inline {
  padding: 0.2em;
  font-weight: 700;
  &:hover {
    border-color: transparent;
    background-color: transparent;
  }
}
</style>
