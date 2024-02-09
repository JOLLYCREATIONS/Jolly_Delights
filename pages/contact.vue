<template>
    <div class="relative w-full h-[50vh] flex flex-col justify-center">
        <img src="/header.webp" class="w-full h-[50vh] object-cover  absolute z-10 top-0">
    </div>
    <div class="mt-8 grid grid-cols-1 md:grid-cols-3  items-center rounded-2xl max-w-7xl mx-auto gap-8">
        <MiscQr v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" :icon="food.icon" />
        <MiscQr v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" :icon="food.icon" />
        <MiscQr v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" :icon="food.icon" />
    </div>
</template>
<script setup lang="ts">
const foods = [
    { name: "PHONE", image: "/qr.png", icon: "M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z" },
    { name: "INSTAGRAM", image: "/qr.png", icon: "M 2 2 L 20 2 L 20 20 L 2 20 L 2 2 Z M 17.5 6.5 L 17.51 6.5 M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z" },
    { name: "YOUTUBE", image: "/qr.png", icon: "M 9.75 15.02 L 15.5 11.75 L 9.75 8.48 L 9.75 15.02 Z M22.54 6.42a2.78 2.78 0 0 0-1.94-2C18.88 4 12 4 12 4s-6.88 0-8.6.46a2.78 2.78 0 0 0-1.94 2A29 29 0 0 0 1 11.75a29 29 0 0 0 .46 5.33A2.78 2.78 0 0 0 3.4 19c1.72.46 8.6.46 8.6.46s6.88 0 8.6-.46a2.78 2.78 0 0 0 1.94-2 29 29 0 0 0 .46-5.25 29 29 0 0 0-.46-5.33z" },
]
</script>