<script setup lang="ts">
import { ref, onMounted } from "vue";
import Sidebar from "@/components/Sidebar/Sidebar.vue";

const container = ref();
const splitter = ref();
const leftPane = ref();
const rightPane = ref();
const isDragging = ref(false);

onMounted(() => {
  splitter.value.addEventListener("mousedown", (e: MouseEvent) => {
    e.preventDefault();
    isDragging.value = true;
    document.addEventListener("mousemove", onMouseMove);
    document.addEventListener("mouseup", onMouseUp);
  });

  function onMouseMove(e: MouseEvent) {
    if (!isDragging.value) return;

    const containerRect = container.value.getBoundingClientRect();
    const offset = e.clientX - containerRect.left;
    const totalWidth = containerRect.width;
    const WIDTH_THRESHOLD = 320;

    const leftWidth = offset;
    const rightWidth = totalWidth - offset - splitter.value.offsetWidth;

    if (leftWidth <= WIDTH_THRESHOLD || rightWidth <= WIDTH_THRESHOLD) return;

    leftPane.value.style.width = `${leftWidth}px`;
    rightPane.value.style.width = `${rightWidth}px`;
  }

  function onMouseUp() {
    isDragging.value = false;
    document.removeEventListener("mousemove", onMouseMove);
    document.removeEventListener("mouseup", onMouseUp);
  }
});
</script>

<template>
  <div class="container" ref="container">
    <div class="pane" ref="leftPane">
      <Sidebar />
    </div>
    <div class="splitter" ref="splitter" />
    <div class="pane" ref="rightPane"></div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.pane {
  background-color: rgba(255, 255, 255, 0.4);
  width: 50%;
  height: 100%;
  border-radius: 1rem;
}

.splitter {
  cursor: ew-resize;
  height: calc(100% - 1.7rem);
  border-radius: 2px;
  padding: 0 4px;
  display: flex;
  align-items: center;

  &:hover {
    &::before {
      opacity: 1;
    }
  }

  &::before {
    content: "";
    display: block;
    opacity: 0;
    width: 2px;
    height: 30%;
    background-color: rgba(255, 255, 255, 0.4);
  }
}
</style>
