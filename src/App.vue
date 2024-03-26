<script setup lang="ts">
import todoButton from '@/components/todoButton.vue';
import todoItem from '@/components/todoItem.vue';
</script>

<template>
  <div class="todo">
    <div class="container">
      <h1 class="todo__title">todo<span>List</span> </h1>
    </div>
  </div>
  <todoButton></todoButton>
  <todoItem></todoItem>
</template>

<style scoped>
.container {
  min-width: 1200px;
  max-width: 1500px;
  margin-top: 8rem;
}

.todo__title {
  color: var(--color-white);
}

.todo__title span {
  font-weight: bold;
  color: var(--color-accent);
}
</style>
