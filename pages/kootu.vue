<template>
    <div class="relative w-full h-[50vh] flex flex-col justify-center">
        <img src="/header banner/3.png" class="w-full h-[50vh] object-cover pt-[1.5rem]  absolute z-10 top-0">
    </div>
    <div class="p-8 mt-8 rounded-xl bg-[#fffff] text-center text-[#000000] font-bold text-6xl w-full">KOOTU</div>
    <div class="p-8 max-w-7xl mx-auto grid grid-cols-3 lg:grid-cols-4 xl:grid-cols-6 items-center mt-15 gap-y-10 gap-8 rounded-2xl">
            <MiscBox v-for="kootus in kootu.concat()" :key="kootus.name" :name="kootus.name" :image="kootus.image" class="mx-auto" />
        </div>
</template>

<script setup lang="ts">
const kootu = [
    { name: "PUDALANGAI KOOTU", image: "/kootu/1.jpg" },
    { name: "POOSANIKAI KOOTU", image: "/kootu/2.jpg" },
    { name: "MIXED VEG KOOTU", image: "/kootu/3.jpg" },
    { name: "CHOW CHOW KOOTU", image: "/kootu/4.jpg" },
    { name: "KOOS KOOTU", image: "/kootu/6.jpg" },
    { name: "BRINJAL KOOTU", image: "/kootu/7.jpg" },
    { name: "AVIAL MALABAR", image: "/kootu/8.jpg" },
    { name: "PARANGIKAI PAAL KOOTU", image: "/kootu/9.jpg" },
    { name: "KADAMBAM KOOTU", image: "/kootu/10.jpg" },
    { name: "SOYACHUNKS KOOTU", image: "/kootu/11.jpg" },
    { name: "VALAKKAI KOOTU", image: "/kootu/12.jpg" },
    { name: "VAZHA PO KOOTU", image: "/kootu/13.jpg" },
    { name: "KEERAI KOOTU", image: "/kootu/14.jpg" },

]
</script>
