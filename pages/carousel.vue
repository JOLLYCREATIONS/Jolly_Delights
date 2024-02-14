<template>
    <div class="relative overflow-hidden">
      <div class="absolute inset-0 flex items-center justify-center">
        <div
          class="w-full h-full flex items-center justify-center transition-transform duration-500 transform"
          :style="`transform: translateX(${-currentIndex * 60}%) rotateY(${-currentIndex * 45}deg);`"
        >
          <div
            v-for="(item, index) in items"
            :key="index"
            class="w-full max-w-xs mx-auto px-4 transform transition-transform duration-500"
            :class="{ 'opacity-100 scale-100': currentIndex === index, 'opacity-0 scale-90': currentIndex !== index }"
          >
            <img :src="item.image" alt="Slider Image" class="w-full rounded-lg shadow-lg" />
          </div>
        </div>
      </div>
      <div class="absolute inset-x-0 bottom-0 flex justify-center mt-4 space-x-2">
        <button
          v-for="(item, index) in items"
          :key="index"
          class="w-4 h-4 rounded-full bg-gray-500 hover:bg-gray-700 focus:outline-none"
          :class="{ 'bg-gray-700': currentIndex === index }"
          @click="currentIndex = index"
        ></button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentIndex: 1,
        items: [
          { image: '/idly.jpg/400x200' },
          { image: '/dosa.jpg/400x200' },
          { image: '/idly.jpg/400x200' },
          { image: '/dosa.jpg/400x200' },
          { image: '/idly.jpg/400x200' },
        ]
      };
    }
  };
  </script>
  
  <style scoped>
  /* Add your Tailwind CSS classes here or import Tailwind's CDN */
  </style>
  