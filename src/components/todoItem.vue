<script setup>
import EditIcon from '@/components/icons/EditIcon.vue';
import CheckboxIcon from "@/components/icons/CheckboxIcon.vue";
import CheckedIcon from "@/components/icons/CheckedIcon.vue";
</script>

<template>
  <div class="todo__item">
    <p class="todo__task">Task text</p>
    <div class="todo__icons">
      <EditIcon class="todo__icon todo__edit-icon"/>
      <CheckboxIcon class="todo__icon"/>
      <CheckedIcon class="todo__icon"/>
    </div>
  </div>

</template>

<style scoped>
.todo__item {
  max-width: 700px;
  min-width: 600px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 20px;
  margin-bottom: 20px;
  background-color: #2f2d36;
  border-radius: 10px;
}

.todo__task {
  color: var(--color-white);
}

.todo__icons {
  display: flex;
}

.todo__icon {
  width: 30px;
  cursor: pointer;
}

.todo__edit-icon {
  margin-right: 0.7rem;
  width: 25px;
  fill: var(--color-white);
}
</style>
