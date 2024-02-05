<template>
    <div class="flex flex-col w-full items-center space-y-12">
        <div class="relative w-full h-screen">
            <video src="/vid.mp4" muted autoplay :controls="false" loop
                class="w-full h-screen object-cover blur-sm absolute z-10"></video>
            <div class="relative z-20 text-2xl text-white">Hello Hello</div>
        </div>
        <div class="p-4 rounded-xl bg-[#CBE7D8] text-white w-full">Popular Items</div>
        <div class="p-4 rounded-xl bg-[#fffff] text-[#206038] font-bold text-2xl w-full">Try Our New Arrivals</div>
        <div class="grid grid-cols-1 lg:grid-cols-2 items-center gap-4">
            <MiscBox v-for = "food in foods" :key="food.name" :name="food.name" :image="food.image" />
        </div>
    </div>
</template>
<script setup lang="ts">
    const foods = [
  {name: "Dosa", image: "/dosa.png"},
  {name: "Idly", image: "/idly.png"},
]
</script>