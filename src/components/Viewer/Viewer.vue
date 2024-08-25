<script setup lang="ts"></script>

<template>
  <header class="header">
    <div class="options"></div>
    <span class="date">21.11.22 at 13:41</span>
    <div class="remove-note"></div>
  </header>
  <textarea class="editor"> </textarea>
</template>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  min-height: 28px;
  margin-bottom: 1rem;
}

.date {
  font-size: 0.75rem; /* 12px */
  line-height: 1rem; /* 16px */
  color: rgba(0, 0, 0, 0.4);
  font-weight: 600;
}

.editor {
  resize: none;
  width: 99%;
  height: 100%;
  border: none;
  display: block;
  border-radius: 1rem;
  background-color: transparent;
  color: #000;
  font-weight: 500;
  font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
}
</style>
