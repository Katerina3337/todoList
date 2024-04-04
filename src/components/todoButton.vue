<script setup>
defineProps({
  buttonText: {
    type: String,
    required: true,
    default: 'Добавить',
  },
  isCancelButton: {
    type: Boolean,
    required: false,
  },
})
</script>

<template>
  <button class="button" :class="{cancel: isCancelButton}">{{ buttonText }}</button>
</template>



<style scoped>
.button {
  font-family: var(--font-main);
  font-size: 15px;
  max-width: 200px;
  min-width: 100px;
  max-height: 45px;
  padding: 8px 20px;
  border-radius: 30px;
  background: linear-gradient(130deg, rgb(157, 137, 224) 0%, rgb(98, 56, 238) 100%);
  color: var(--color-white);
  border: none;
  cursor: pointer;
}

.cancel {
  background: linear-gradient(130deg, rgb(250, 97, 97) 0%, rgb(220, 27, 27) 100%);
}

.button:hover {
  box-shadow: 0 0 5px rgba(192, 91, 243, 0.77);
}

.cancel:hover {
  box-shadow: 0 0 5px rgba(243, 91, 91, 0.77);
}
</style>
