<template>
    <div class="relative w-full h-screen flex flex-col justify-center">
        <img src="/header.webp" class="w-full h-screen object-cover  absolute z-10">
    </div>
    <div class="grid grid-cols-1 lg:grid-cols-2 lg:grid-cols-3 items-center rounded-2xl gap-8">
            <MiscQr v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
            <MiscQr v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
            <MiscQr v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
        </div>
</template>
<script setup lang="ts">
const foods = [
    { name: "PHONE", image: "/qr.png" },
    { name: "INSTAGRAM", image: "/qr.png" },
    { name: "YOUTUBE", image: "/qr.png" },
]
</script>