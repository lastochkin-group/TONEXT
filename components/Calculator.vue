<template>
    <section class="py-12 bg-gray-100 text-center">
      <h2 class="text-2xl font-bold mb-4">Калькулятор</h2>
      <div class="max-w-md mx-auto bg-white p-6 rounded shadow">
        <form>
          <div class="mb-4">
            <label for="investment" class="block text-left">Сумма инвестиции:</label>
            <input type="number" id="investment" class="w-full px-3 py-2 border rounded"/>
          </div>
          <div class="mb-4">
            <label for="days" class="block text-left">Срок (дней):</label>
            <input type="number" id="days" class="w-full px-3 py-2 border rounded"/>
          </div>
          <button class="bg-blue-500 text-white px-4 py-2 rounded">Рассчитать</button>
        </form>
      </div>
    </section>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  /* Custom styles for the calculator if needed */
  </style>
  