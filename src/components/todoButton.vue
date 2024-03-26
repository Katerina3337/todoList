<template>
  <button class="button">Кнопка</button>
</template>

<style scoped>
.button {
  font-family: var(--font-main);
  font-size: 15px;
  max-width: 300px;
  min-width: 100px;
  max-height: 45px;
  padding: 8px 20px;
  border-radius: 30px;
  background: linear-gradient(130deg, rgb(157, 137, 224) 0%, rgb(98, 56, 238) 100%);
  color: var(--color-white);
  border: none;
  cursor: pointer;
}

.button:hover {
  box-shadow: 0 0 5px rgba(192, 91, 243, 0.77);
}
</style>
