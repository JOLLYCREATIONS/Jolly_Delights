<template>
    <div class="relative w-full h-[50vh] flex flex-col justify-center">
        <img src="/header.webp" class="w-full h-[50vh] object-cover  absolute z-10 top-0">
    </div>
    <div class="p-4 mt-8 rounded-xl bg-[#fffff] text-center text-[#000000] font-bold text-6xl w-full">PAYASAM</div>
    <div class="p-8 grid grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 items-center mt-5 gap-8 rounded-2xl">
            <MiscBox v-for="payasams in payasam.concat()" :key="payasams.name" :name="payasams.name" :image="payasams.image" class="mx-auto" />
        </div>
</template>

<script setup lang="ts">
const payasam = [
    { name: "ELANEER PAYASAM", image: "/payasam/elaneer_payasam.jpg" },
    { name: "PALADA PAYASAM", image: "/payasam/palada_payasam.jpg" },
    { name: "SEMIYA PAYASAM", image: "/payasam/semiya_payasam.jpg" },
    { name: "FRUIT PAYASAM", image: "/payasam/fruit_payasam.jpg" },
    { name: "PAL PAYASAM", image: "/payasam/pal_payasam.jpg" },
    { name: "PARUPPU PAYASAM", image: "/payasam/paruppu_payasam.jpg" },
    { name: "BADAM KHEER", image: "/payasam/badam_kheer.jpg" },
    { name: "ADAI PRATHAMAN PAYASAM", image: "/payasam/adai_prathaman_payasam.jpg" },
    { name: "PALADAI PRATHAMAN PAYASAM", image: "/payasam/paladai_prathaman_payasam.jpg" },
    { name: "JAVARSI PAYASAM", image: "/payasam/javarsi_payasam.jpg" },
    { name: "CARROT KHEER", image: "/payasam/carrot_kheer.jpg" },
    { name: "ARISI PAYASAM", image: "/payasam/arisi_payasam.jpg" },
    { name: "PACHA ARISI PAYASAM", image: "/payasam/pacha_arisi_payasam.jpg" },
    { name: "GOTHUMAI RAVA PAYASAM", image: "/payasam/gothumai_rava_payasam.jpg" },
    { name: "AKARA VADISAL PAYASAM", image: "/payasam/akara_vadisal_payasam.jpg" },
]
</script>
