<template>
    <div class="flex flex-col w-full items-center space-y-12">
        <div class="relative w-full h-screen flex flex-col justify-center">
            <video src="/vid.mp4" muted autoplay :controls="false" loop
                class="w-full h-screen object-cover  absolute z-10"></video>
            <div class="relative z-20  text-6xl text-white px-4">Want to taste something Delicious</div>
        </div>
        <div class="p-4 rounded-xl bg-[#CBE7D8] text-white w-full">Popular Items</div>
        <div class="p-4 rounded-xl bg-[#fffff] text-[#206038] font-bold text-6xl w-full">Try Our New Arrivals</div>
        <div class="grid grid-cols-1 lg:grid-cols-2 lg:grid-cols-3 lg:grid-cols-4 items-center rounded-2xl gap-8">
            <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-2 lg:grid-cols-3 lg:grid-cols-4 rounded-2xl items-center gap-8">
            <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
        </div>
        <div class="p-4 rounded-xl bg-[#CBE7D8] text-black text-2xl ">Search By Food
            <div class="grid grid-cols-1 lg:grid-cols-2 lg:grid-cols-3 lg:grid-cols-4 items-center  gap-8">
                <MiscCircle v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
            </div>
            <div class="grid grid-cols-1 lg:grid-cols-2 lg:grid-cols-3 lg:grid-cols-4 items-center  gap-8">
                <MiscCircle v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
            </div>
        </div>

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