<script setup lang="ts">
import { ref } from "vue";

interface Item {
  title: string;
  onClick: () => null;
  active: boolean;
}

const items = ref([
  {
    title: "All",
    onClick: () => null,
    active: true,
  },
  {
    title: "Done",
    onClick: () => null,
    active: false,
  },
  {
    title: "Undone",
    onClick: () => null,
    active: false,
  },
  {
    title: "In Progress",
    onClick: () => null,
    active: false,
  },
]);

const setActive = (title: string) => {
  items.value = items.value.map((prevItem: Item) => ({
    ...prevItem,
    active: prevItem.title === title,
  }));
};
</script>

<template>
  <div class="scroll-wrapper">
    <div class="selector">
      <template v-for="(item, index) in items" :key="item.title">
        <div
          class="option"
          :class="{ active: item.active }"
          @click="setActive(item.title)"
        >
          {{ item.title }}
        </div>
        <div v-if="index < items.length - 1" class="divider"></div>
      </template>
    </div>
  </div>
</template>

<style scoped lang="scss">
.scroll-wrapper {
  overflow: scroll;
  border-radius: 8px;
  background-color: rgba(255, 255, 255, 0.3);
}

.selector {
  width: 100%;
  display: flex;
  align-items: center;
  border-radius: 8px;
  gap: 6px;
}

.option {
  min-height: 32px;
  display: flex;
  width: 100%;
  justify-content: center;
  align-items: center;
  border-radius: 8px;
  padding: 0 18px;
  color: #000;
  font-weight: 600;
  cursor: pointer;
  white-space: nowrap;
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
