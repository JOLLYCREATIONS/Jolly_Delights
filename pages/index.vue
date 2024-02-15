<template>
    <div class="flex flex-col w-full items-center space-y-12">
        <div class="relative w-full h-screen flex flex-col justify-center">
            <video src="/vid.mp4" muted autoplay :controls="false" loop
                class="w-full h-screen object-cover  absolute z-10"></video>
            <div class="relative z-20  text-6xl text-white px-4">Want to taste something Delicious</div>
        </div>
        <div class="max-w-7xl mx-auto flex flex-col gap-12">
            <div class="p-4 rounded-xl bg-[#CBE7D8] text-white w-full">Popular Items</div>
            <div><span class="font-bold text-xl md:text-3xl lg:text-4xl text-[#206038]">Try Our New Arrivals</span>
                <div class="grid grid-cols-1 lg:grid-cols-2 lg:grid-cols-3 lg:grid-cols-4 items-center mt-5 gap-8">
                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
                </div>
            </div>
            <div class="p-4 rounded-3xl bg-[#CBE7D8] text-black text-2xl ">
                <div class="p-4 w-full flex items-center gap-4">
                    <svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 24 24" fill="none"
                        stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"
                        class="feather feather-search">
                        <circle cx="11" cy="11" r="8"></circle>
                        <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
                    </svg><span class="text-black font-bold text-xl md:text-3xl lg:text-4xl">Search By Category</span>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-5  md:grid-cols-4 items-center mt-5  gap-8">
                    <MiscCircle v-for="food in menu" :key="food.name" :name="food.name" :image="food.image" />
                    <MiscCircle v-for="food in menu" :key="food.name" :name="food.name" :image="food.image" />
                </div>
            </div>
            <div><span class="font-bold text-xl md:text-3xl lg:text-4xl text-[#206038]">Customer Testimonials</span>
                <MiscCarosuel class="mt-5" :images="reviews"></MiscCarosuel>
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
const menu = [
    { name: "Dosa", image: "/dosa.jpg" },
    { name: "Idly", image: "/idli.jpg" },
    { name: "Idly", image: "/idli.jpg" },
    { name: "Parotta", image: "/parotta.jpg" },
    { name: "Dosa", image: "/dosa.jpg" },
]

const reviews = [
    {
        name: "Joseph Stalin",
        review: "Excellent North Indian food at affordable prices... Roti Thali is one of the best options imo but you can get nice noodles of different variety too",
        ratings: 4.5,
    },
    {
        name: "Qin Shi Huang",
        review: "Very good food I will always come here",
        ratings: 5,
    },
    {
        name: "Joseph Stalin",
        review: "Excellent North Indian food at affordable prices... Roti Thali is one of the best options imo but you can get nice noodles of different variety too",
        ratings: 4.5,
    },
    {
        name: "Qin Shi Huang",
        review: "Very good food I will always come here",
        ratings: 5,
    },
    {
        name: "Joseph Stalin",
        review: "Excellent North Indian food at affordable prices... Roti Thali is one of the best options imo but you can get nice noodles of different variety too",
        ratings: 4.5,
    },
    {
        name: "Qin Shi Huang",
        review: "Very good food I will always come here",
        ratings: 5,
    },
]
</script>