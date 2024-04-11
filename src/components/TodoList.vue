<script setup>
import TodoItem from '@/components/TodoItem.vue';
import TodoButton from '@/components/TodoButton.vue';
import TodoModal from '@/components/TodoModal.vue';
import {ref} from "vue";

const isShowModal = ref(false);
const buttonText = ref('Добавить');
const showModal = () => {
  isShowModal.value = true;
}
const closeModal = () => {
  isShowModal.value = false;
}
</script>

<template>
  <div class="todo__tasks">
    <h3 class="todo__title">Задачи</h3>
    <TodoItem></TodoItem>
    <TodoModal
        v-if="isShowModal"
        :button-text="buttonText"
        @close-modal="closeModal"
    />
    <div>
      <TodoButton class="todo__button" @click="showModal"></TodoButton>
    </div>
  </div>
</template>

<style scoped>
.todo__tasks {
  display: flex;
  flex-direction: column;
  min-height: 500px;
  max-width: 765px;
  min-width: 765px;
  padding: 20px 30px;
  position: relative;
  background-color: #18181c;
  border-radius: 15px;
}

.todo__title {
  margin-bottom: 15px;
  color: var(--color-title);
}

.todo__button {
  position: absolute;
  bottom: 25px;
  right: 25px;
}

</style>
