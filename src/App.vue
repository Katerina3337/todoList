<script setup lang="ts">
import todoList from '@/components/todoList.vue';
import todoFilters from '@/components/todoFilters.vue';

</script>

<template>
  <div class="todo">
    <div class="container">
      <h1 class="todo__title">todo<span>List</span></h1>
      <div class="todo__tabs">
        <todoFilters></todoFilters>
        <todoList></todoList>
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
