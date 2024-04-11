<script setup lang="ts">
import TodoList from '@/components/TodoList.vue';
import TodoFilters from '@/components/TodoFilters.vue';

</script>

<template>
  <div class="todo">
    <div class="container">
      <h1 class="todo__title">todo<span>List</span></h1>
      <div class="todo__tabs">
        <TodoFilters></TodoFilters>
        <TodoList></TodoList>
      </div>
    </div>
  </div>

</template>

<style scoped>
.container {
  min-width: 1200px;
  max-width: 1500px;
  margin-top: 8rem;
}

.todo__title {
  margin-bottom: 45px;
  color: var(--color-white);
}

.todo__title span {
  font-weight: bold;
  color: var(--color-accent);
}

.todo__tabs {
  display: flex;
  justify-content: space-between;
}
</style>
