<template>
    <div class="p-6 bg-gray-50 rounded-lg shadow-md border border-gray-200">
      <!-- First Slider -->
      <div class="flex items-center space-x-4 mb-6">
        <div class="flex items-center space-x-2 bg-white p-2 rounded-full shadow-md">
          <img src="" alt="Icon" class="w-6 h-6"/>
          <span>85</span>
        </div>
        <input type="range" class="flex-grow slider" />
        <button class="bg-gray-200 px-4 py-2 rounded-full">Макс</button>
      </div>
      
      <!-- Second Slider -->
      <div class="flex items-center space-x-4 mb-6">
        <div class="flex items-center space-x-2 bg-white p-2 rounded-full border border-blue-300 shadow-md">
          <img src="" alt="Icon" class="w-6 h-6"/>
          <span>85</span>
        </div>
        <input type="range" class="flex-grow slider" />
        <button class="bg-gray-200 px-4 py-2 rounded-full">Макс</button>
      </div>
      
      <!-- Third Slider -->
      <div class="flex items-center space-x-4 mb-6">
        <div class="flex items-center space-x-2 bg-white p-2 rounded-full shadow-md border border-blue-400">
          <img src="" alt="Icon" class="w-6 h-6"/>
          <span>15,190,325</span>
        </div>
        <input type="range" class="flex-grow slider" />
        <button class="bg-blue-100 text-blue-600 px-4 py-2 rounded-full">Макс</button>
      </div>
      
      <!-- Fourth Slider -->
      <div class="flex items-center space-x-4">
        <div class="flex items-center space-x-2 bg-gray-200 p-2 rounded-full shadow-md">
          <img src="" alt="Icon" class="w-6 h-6 opacity-50"/>
          <span class="opacity-50">85</span>
        </div>
        <input type="range" class="flex-grow slider" disabled />
        <button class="bg-gray-200 px-4 py-2 rounded-full opacity-50">Макс</button>
      </div>
    </div>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .slider {
    -webkit-appearance: none;
    width: 100%;
    height: 4px;
    background: #ccc;
    outline: none;
    opacity: 0.7;
    transition: opacity .2s;
  }
  
  .slider:hover {
    opacity: 1;
  }
  
  .slider::-webkit-slider-thumb {
    -webkit-appearance: none;
    appearance: none;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background: #4CAF50;
    cursor: pointer;
  }
  
  .slider::-moz-range-thumb {
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background: #4CAF50;
    cursor: pointer;
  }
  </style>
  