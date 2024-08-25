<script setup lang="ts"></script>

<template>
  <div class="note">
    <div class="info">
      <div class="title">Lorem ispum <span class="date">21.11.22</span></div>
      <div class="description">
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Vero eaque
        vitae quidem perspiciatis, minus nesciunt error tenetur maiores quis!
        Voluptate officiis ipsa voluptatum id fuga maiores doloremque assumenda
        sapiente possimus!
      </div>
    </div>
    <div class="status">Done</div>
  </div>
</template>

<style lang="scss" scoped>
.note {
  display: flex;
  padding: 16px;
  justify-content: space-between;
  align-items: center;
  border-radius: 16px;
  background-color: rgba(255, 255, 255, 0.3);
  color: #000;
}

.info {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.title {
  font-size: 1.125rem; /* 18px */
  line-height: 1.75rem; /* 28px */
  font-weight: 700;
  display: flex;
  align-items: center;
  gap: 10px;
}

.date {
  color: rgba(0, 0, 0, 0.3);
  font-size: 0.75rem; /* 12px */
  line-height: 1rem; /* 16px */
  margin-top: 3px;
}

.description {
  font-size: 0.875rem; /* 14px */
  line-height: 1.25rem; /* 20px */
  overflow: hidden;
  white-space: nowrap;
  max-width: 300px;
  text-overflow: ellipsis;
}
</style>
