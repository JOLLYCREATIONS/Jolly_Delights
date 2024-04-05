<template>
    <div class="relative w-full h-[50vh] flex flex-col justify-center">
        <img src="/header banner/3.png" class="w-full h-[50vh] object-cover  absolute z-10 top-0">
    </div>
    <div class="p-8 mt-8 rounded-xl bg-[#fffff] text-center text-[#000000] font-bold text-6xl w-full">IDLY</div>
    <div class="p-8 max-w-7xl mx-auto grid grid-cols-3 lg:grid-cols-4 xl:grid-cols-6 items-center mt-15 gap-y-10 gap-8 rounded-2xl">
            <MiscBox v-for="idlis in idli.concat()" :key="idlis.name" :name="idlis.name" :image="idlis.image" class="mx-auto" />
        </div>
</template>

<script setup lang="ts">
const idli = [
    { name: "IDLY", image: "/idly/42.jpg" },
    { name: "MUSHROOM IDLY", image: "/idly/43.jpg" },
    { name: "MALI IDLY", image: "/idly/44.jpg" },
    { name: "VEGETABLE IDLY", image: "/idly/45.jpg" },
    { name: "ELANEER IDLY", image: "/idly/46.jpg" },
    { name: "CARROT IDLY", image: "/idly/47.jpg" },
    { name: "BANGALORE THATTE IDLY", image: "/idly/48.jpg" },
    { name: "TALIPU IDLY", image: "/idly/49.jpg" },
    { name: "HEARTIN IDLY", image: "/idly/50.jpg" },
    { name: "RAVA IDLY", image: "/idly/51.jpg" },
    { name: "KANCHIPURAM IDLY", image: "/idly/52.jpg" },
    { name: "KUSHBOO IDLY", image: "/idly/53.jpg" },
    { name: "MASALA IDLY", image: "/idly/54.jpg" },
    { name: "PODI IDLY", image: "/idly/55.jpg" },
    { name: "FRIED IDLY", image: "/idly/56.jpg" },
    { name: "MINI IDLY SAMBAR", image: "/idly/57.jpg"},
    { name: "PUDINA IDLY", image: "/idly/58.jpg"},
    { name: "GLASS IDLY", image: "/idly/59.jpg" },
    { name: "MINI PODI IDLY", image: "/idly/60.jpg" },

]
</script>
