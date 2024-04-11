<script setup>
import TodoFilter from '@/components/TodoFilter.vue';
</script>

<template>
  <div class="todo__filters">
    <h3 class="todo__filters-title">Фильтры</h3>
    <TodoFilter></TodoFilter>
  </div>

</template>

<style scoped>
.todo__filters {
  display: flex;
  flex-direction: column;
  min-height: 500px;
  width: 390px;
  padding: 20px 30px;
  background-color: #18181c;
  border-radius: 15px;
}

.todo__filters-title {
  margin-bottom: 15px;
  color: var(--color-title);
}
</style>
