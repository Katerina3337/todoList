<script setup>
import TodoButton from "@/components/TodoButton.vue";
import CancelIcon from '@/components/icons/CancelIcon.vue';

defineProps({
  buttonText: {
    type: String,
    required: true,
    default: 'Добавить',
  },
  isShowModal: {
    type: Boolean,
  }
})
</script>

<template>
<div class="todo__modal-layout">
  <div class="todo__modal">
    <CancelIcon class="todo__icon" @click="$emit('closeModal')"/>
    <div class="todo__modal--text-field">
      <label class="todo__modal--label" for="title">Название задачи</label>
      <input class="todo__modal--input" type="text">
    </div>
    <div class="todo__modal--text-field">
      <label class="todo__modal--label" for="title">Описание задачи</label>
      <textarea class="todo__modal--textarea" type="text" rows="10"></textarea>
    </div>
    <div class="todo__buttons">
      <todo-button class="todo__modal--button" :button-text="buttonText"/>
      <todo-button button-text="Отмена" :is-cancel-button="true" @click="$emit('closeModal')"/>
    </div>
  </div>
</div>
</template>

<style scoped>
.todo__modal-layout {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;

  background-color: rgba(30, 22, 49, 0.7);
  display: flex;
  justify-content: center;
  align-items: center;
}

.todo__modal {
  display: flex;
  flex-direction: column;
  width: 600px;
  height: 450px;
  padding: 30px;
  position: relative;
  background-color: #404062;
  border-radius: 30px;
}

.todo__modal--text-field {
  margin-bottom: 1.5rem;
  display: flex;
  flex-direction: column;
}

.todo__modal--label {
  color: #cabbe8;
}

.todo__modal--input {
  min-height: 40px;
}

.todo__modal--input,
.todo__modal--textarea {
  padding: 10px;
  outline: none;
  font-size: 15px;
  background-color: #cabbe8;
  color: var(--color-accent);
  border: none;
  border-radius: 10px;
}

.todo__buttons {
  margin-top: 1.5rem;
  margin-left: auto;
}

.todo__icon {
  position: absolute;
  top: 10px;
  right: 15px;
  fill: #cabbe8;
}

.todo__modal--button {
  margin-right: 25px;
}
</style>
