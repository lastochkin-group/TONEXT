<template>
    <div>
      <header class="text-center py-24 bg-blue-600 text-white">
        <h1 class="text-4xl font-bold mb-4">Начните зарабатывать до 4% ежедневно</h1>
        <p class="mb-8">Децентрализированный Liquid Staking TON</p>
        <button class="bg-white text-blue-600 px-6 py-3 rounded font-semibold">Начать сейчас</button>
      </header>
      <Calculator />
      <Steps />
      <Advantages />
      <Faq />
    </div>
  </template>
  
  <script setup>
  import Calculator from '@/components/Calculator.vue'
  import Steps from '@/components/Steps.vue'
  import Advantages from '@/components/Advantages.vue'
  import Faq from '@/components/Faq.vue'
  </script>
  
  <style scoped>
  /* Custom styles for the main page if needed */
  </style>
  