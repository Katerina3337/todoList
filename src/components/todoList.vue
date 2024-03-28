<script setup>
import todoItem from '@/components/todoItem.vue';
import todoButton from '@/components/todoButton.vue';
</script>

<template>
  <div class="todo__tasks">
    <h3 class="todo__title">Задачи</h3>
    <todoItem></todoItem>
    <div>
      <todoButton class="todo__button"></todoButton>
    </div>
  </div>
</template>

<style scoped>
.todo__tasks {
  display: flex;
  flex-direction: column;
  max-width: 780px;
  min-width: 780px;
  padding: 20px 30px;
  background-color: #18181c;
  border-radius: 15px;
}

.todo__title {
  margin-bottom: 15px;
  color: var(--color-title);
}

.todo__button {
  float: right;
}

</style>
