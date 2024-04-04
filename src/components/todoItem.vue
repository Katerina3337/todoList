<script setup>
import EditIcon from '@/components/icons/EditIcon.vue';
import CheckboxIcon from "@/components/icons/CheckboxIcon.vue";
import CheckedIcon from "@/components/icons/CheckedIcon.vue";
import TodoModal from '@/components/TodoModal.vue';

import { ref } from 'vue';

const isShowModal = ref(false);
const buttonText = ref('Редактировать');
const showModal = () => {
  isShowModal.value = true;
}
const closeModal = () => {
  isShowModal.value = false;
}
</script>

<template>
  <div class="todo__item">
    <p class="todo__task">Task text</p>
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
