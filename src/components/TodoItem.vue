<script setup>
import EditIcon from '@/components/icons/EditIcon.vue';
import CheckboxIcon from "@/components/icons/CheckboxIcon.vue";
import CheckedIcon from "@/components/icons/CheckedIcon.vue";
import CircleIcon from '@/components/icons/CircleIcon.vue';
import CircleCheckedIcon from '@/components/icons/CircleCheckedIcon.vue';
import TodoModal from '@/components/TodoModal.vue';

import { ref } from 'vue';

defineProps({
  todoItem: {
    type: Object,
    required: true,
  }
})

const isShowModal = ref(false);
const buttonText = ref('Редактировать');
const isTaskDone = ref(false);

const changeTaskStatus = () => {
  isTaskDone.value = !isTaskDone.value;
}

const showModal = () => {
  isShowModal.value = true;
}
const closeModal = () => {
  isShowModal.value = false;
}
</script>

<template>
  <div class="todo__item" :class="{'done-task': isTaskDone}">
    <div class="todo__task-wrapper">
      <div class="todo__icons">
        <CircleIcon class="todo__icon" v-if="!isTaskDone" @click="changeTaskStatus"/>
        <CircleCheckedIcon class="todo__icon" v-else @click="changeTaskStatus"/>
      </div>
      <p class="todo__task">{{ todoItem.title }}</p>
    </div>
    <div class="todo__icons">
      <EditIcon class="todo__icon todo__edit-icon" @click="showModal"/>
      <CheckboxIcon class="todo__icon todo__delete-icon"/>
      <CheckedIcon class="todo__icon todo__delete-icon"/>
      <TodoModal
          v-if="isShowModal"
          :button-text="buttonText"
          :is-show-modal="isShowModal"
          @close-modal="closeModal"
      />
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

.done-task {
  opacity: 0.5;
}

.todo__task-wrapper {
  display: flex;
  align-items: center;
}

.todo__icons {
  margin-right: 1rem;
}

.todo__icon {
  fill: var(--color-filter-text);
}

.todo__task {
  color: var(--color-white);
}

.todo__edit-icon {
  margin-right: 0.7rem;
  width: 20px;
  fill: var(--color-white);
}

.todo__delete-icon {
  fill: var(--color-danger);
}
</style>
