<template>
    <div class="relative w-full h-screen flex flex-col justify-center">
        <img src="/header.webp" class="w-full h-screen object-cover  absolute z-10">
    </div>
    <div class="p-4 rounded-xl bg-[#fffff] text-[#000000] font-bold text-6xl w-full">ITEMS</div>
    <div class="grid grid-cols-1 lg:grid-cols-2 lg:grid-cols-3 lg:grid-cols-4 items-center rounded-2xl gap-8">
            <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
            <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
            <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
            <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
        </div>

</template>
<script setup lang="ts">
const foods = [
    { name: "Dosa", image: "/dosa.jpg" },
    { name: "Idly", image: "/idli.jpg" },
    { name: "Idly", image: "/idli.jpg" },
    { name: "Parotta", image: "/parotta.jpg" },
]
</script>