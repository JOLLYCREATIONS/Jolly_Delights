<template>
    <div class="relative w-full h-[50vh] flex flex-col justify-center">
        <img src="/header.webp" class="w-full h-[50vh] object-cover  absolute z-10 top-0">
    </div>
    <div class="p-4 mt-8 rounded-xl bg-[#fffff] text-center text-[#000000] font-bold text-6xl w-full">ITEMS</div>
    <div class="mt-8 grid grid-cols-1 md:grid-cols-3 lg:grid-cols-5 items-center rounded-2xl max-w-7xl mx-auto gap-8">
            <MiscBox v-for="food in foods.concat(foods.concat(foods.concat(foods.concat(foods))))" :key="food.name" :name="food.name" :image="food.image" class="mx-auto" />
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