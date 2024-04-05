<template>
    <div class="relative w-full h-[50vh] flex flex-col justify-center">
        <img src="/header banner/1.png" class="w-full h-[50vh] object-cover  absolute z-10 top-0">
    </div>
    <div class="p-8 mt-8 rounded-xl bg-[#fffff] text-center text-[#000000] font-bold text-6xl w-full">SWEETS</div>
    <div class="p-8 max-w-8xl mx-auto grid grid-cols-3 lg:grid-cols-4 xl:grid-cols-6 items-center mt-15 gap-y-10 gap-8 rounded-2xl">
            <MiscBox v-for="idlis in idli.concat()" :key="idlis.name" :name="idlis.name" :image="idlis.image" class="mx-auto" />
        </div>
</template>

<script setup lang="ts">
const idli = [
    { name: "GULAB JAMMUN", image: "/sweets/1.jpg" },
    { name: "MAKKAN BEDA", image: "/sweets/2.jpg" },
    { name: "DRY JAMUN", image: "/sweets/3.jpg" },
    { name: "RAS MALAI", image: "/sweets/4.jpg" },
    { name: "AGRA PAN", image: "/sweets/5.jpg" },
    { name: "KHOYA BARFI", image: "/sweets/6.jpg" },
    { name: "THENGAI POLI", image: "/sweets/7.jpg" },
    { name: "MALAI SANDWICH", image: "/sweets/8.jpg" },
    { name: "CHUM CHUM", image: "/sweets/9.jpg" },
    { name: "ANGOOR RAPPADI", image: "/sweets/10.jpg" },
    { name: "LYCHEE RABDI", image: "/sweets/11.jpg" },
    { name: "KALA JAMMUN", image: "/sweets/12.jpg" },
    { name: "BADUSHA", image: "/sweets/13.jpg" },
    { name: "MINI JILEBI", image: "/sweets/14.jpg" },
    { name: "PARUPU POLI", image: "/sweets/15.jpg" },
    { name: "JILEBI", image: "/sweets/16.jpg"},
    { name: "DRY FRUIT BARFI", image: "/sweets/17.jpg"},
    { name: "MALAI SUM SUM", image: "/sweets/18.jpg" },
    { name: "LADDU", image: "/sweets/19.jpg" },
    { name: "KAJU KATHLI", image: "/sweets/20.jpg" },
    { name: "COLOR BOONDI", image: "/sweets/21.jpg" },
    { name: "ANJEER ROLL", image: "/sweets/22.jpg" },
    { name: "PHENI", image: "/sweets/23.jpg" },
    { name: "KAJU KAMAL", image: "/sweets/24.jpg" },
    { name: "AGRA PETHA", image: "/sweets/25.jpg" },
    { name: "BADAM KATLI", image: "/sweets/26.jpg" },
    { name: "KAJU PISTA ROLL", image: "/sweets/27.jpg" },
    { name: "MYSORE PAK", image: "/sweets/28.jpg" },
    { name: "KASHI HALWA", image: "/sweets/29.jpg" },
    { name: "CARROT HALWA", image: "/sweets/30.jpg" },
    { name: "BADAM HALWA", image: "/sweets/31.jpg" },
    { name: "WHEAT HALWA", image: "/sweets/32.jpg" },
    { name: "BREAD HALWA", image: "/sweets/33.jpg" },
    { name: "ASHOKA HALWA", image: "/sweets/34.jpg" },
    { name: "PINAPPLE KESARI", image: "/sweets/35.jpg" },
    { name: "MILK KESARI ", image: "/sweets/36.jpg" },
    { name: "RAJBHOG", image: "/sweets/37.jpg" },
    { name: "RASGULLA", image: "/sweets/38.jpg" },
    { name: "MALAI ROLL", image: "/sweets/39.jpg" },
    { name: "BADAM ROLL", image: "/sweets/40.jpg" },
    { name: "SPL PISTA ROLL", image: "/sweets/41.jpg" },
    { name: "MALPUA", image: "/sweets/42.jpg" },
    { name: "MILK KALAKAND", image: "/sweets/43.jpg" },
]
</script>