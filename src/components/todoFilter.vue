<script setup>
import CircleIcon from '@/components/icons/CircleIcon.vue';
import CircleCheckedIcon from '@/components/icons/CircleCheckedIcon.vue';
</script>

<template>
  <div class="todo__filter">
    <div class="todo__icons">
      <CircleIcon class="todo__icon"></CircleIcon>
      <CircleCheckedIcon class="todo__icon"/>
    </div>
    <p class="todo__filter-text">dvvdvdr</p>
  </div>
</template>

<style scoped>
.todo__filter {
  max-width: 700px;
  min-width: 300px;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  padding: 10px 20px;
  margin-bottom: 20px;
  background-color: #2f2d36;
  border-radius: 10px;
}

.todo__icon {
  fill: var(--color-filter-text);
}

.todo__filter-text {
  margin-left: 10px;
  color: var(--color-filter-text);
}
</style>
