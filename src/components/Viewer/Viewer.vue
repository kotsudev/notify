<script setup lang="ts">
import ViewerHeader from "@/components/Viewer/ViewerHeader.vue";
</script>

<template>
  <ViewerHeader />
  <textarea class="editor"> </textarea>
</template>

<style lang="scss" scoped>
.editor {
  resize: none;
  width: 99%;
  height: 100%;
  border: none;
  display: block;
  border-radius: 8px;
  background-color: transparent;
  color: #000;
  font-weight: 500;
  font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
}
</style>
