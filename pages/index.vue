<template>
    <div class="flex flex-col relative w-full items-center space-y-12">
        <div class="relative w-full h-screen flex flex-col justify-start">
            <video src="/promo.mp4" muted autoplay :controls="false" loop
                class="w-full h-screen object-cover  absolute z-10"></video>
            <div class="absolute z-20 w-full bottom-10 flex flex-col-reverse items-center justify-center gap-8">
                <button class="w-20 h-20 relative" @click="scrollToMain">
                    <div
                        class="w-16 h-16 mx-auto p-2 uppercase bg-[#CBE7D8] transition ease-in-out border-green-800 border-4 text-black hover:bg-[#ffcf03] font-black text-sm rounded-full flex items-center gap-2">

                        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none"
                            stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                            class="feather feather-chevron-right mx-auto">
                            <polyline points="18 6 12 12 6 6" class="bounceAlpha" style="animation-delay:0.2s;"></polyline>
                            <polyline points="18 17 12 23 6 17" class="bounceAlpha"></polyline>
                        </svg>
                    </div>
                </button>
                <a href="#" class="relative w-16 h-16">
                    <div
                        class="inset-0 p-2 uppercase bg-[#CBE7D8] hover:bg-[#ffcf03] transition ease-in-out duration 600 hover:scale-105  border-green-800 border-4 text-black font-black text-sm rounded-full flex items-center gap-2 absolute z-10 mx-auto">
                        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"
                            fill="#206038" stroke="none" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                            class="feather mx-auto">
                            <path
                                d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z">
                            </path>
                        </svg>
                    </div>
                    <div
                        class="inset-0 p-2 uppercase bg-[#CBE7D8]  transition ease-in-out duration 600 hover:scale-105  border-green-800 border-4 text-black font-black text-sm rounded-full flex items-center gap-2 absolute z-0 mx-auto animate-ping">
                        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"
                            fill="#206038" stroke="currentColor" stroke-width="2" stroke-linecap="round"
                            stroke-linejoin="round" class="feather">
                            <path
                                d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z">
                            </path>
                        </svg>
                    </div>
                </a>
            </div>
        </div>
        <div class="w-full p-8 flex flex-col gap-12" id="main-content">
            <div class="h-screen flex flex-col justify-center">
                <div class="p-6 rounded-3xl bg-[#CBE7D8]   text-black text-2xl ">
                    <div class="p-2 w-full flex items-center gap-4">
                        <span
                            class="text-black font-bold text-xl md:text-3xl lg:text-4xl text-center underline mx-auto">Popular
                            Items</span>
                    </div>
                    <MiscCards :items="foods.concat(foods.concat(foods))" />
                    <button
                        class="p-2 uppercase bg-[#ffcf03] transition ease-in-out hover:bg-green-800 hover:text-white text-black font-black text-sm mb-8 rounded-lg flex items-center gap-2 mx-auto">

                        <span>Order Now</span>

                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none"
                            stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                            class="feather feather-chevron-right">
                            <polyline points="9 18 15 12 9 6"></polyline>
                        </svg>
                    </button>
                </div>
            </div>
        </div>

        <div class="min-h-screen flex flex-col w-full justify-center bg-contain bg-no-repeat bg-center"
            style="background-image: url(/bg/5.jpg);">
            <div class="mx-auto max-w-7xl"><span class="font-bold text-xl md:text-3xl  lg:text-4xl text-[#206038]">Try
                    Our New Arrivals</span>
                <div class="grid grid-cols-3 md:grid-cols-4 lg:grid-cols-5 xl:grid-cols-5 items-center mt-5 gap-4">
                    <MiscBox v-for="food in trymenu.concat(trymenu)" :key="food.name" :name="food.name"
                        :image="food.image" :ratings="food.ratings" />
                </div>
            </div>
        </div>
        <div class="min-h-screen w-full p-4 flex flex-col justify-center">
            <div class="p-4">
                <div class="rounded-3xl bg-[#CBE7D8] p-2 text-black text-2xl ">
                    <div class="p-4 w-full flex items-center gap-4">
                        <svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 24 24" fill="none"
                            stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"
                            class="feather feather-search">
                            <circle cx="11" cy="11" r="8"></circle>
                            <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
                        </svg><span class="text-black font-bold text-xl md:text-3xl lg:text-4xl">Search By
                            Category</span>
                    </div>

                    <div class="grid grid-cols-1 lg:grid-cols-8  md:grid-cols-6 items-center mt-5  gap-5 ">
                        <a v-for="food in menu.concat(menu.concat(menu.concat()))" :key="food.name" :href="food.link">
                            <MiscCircle :name="food.name" :image="food.image" />
                        </a>
                    </div>
                </div>
            </div>
        </div>
        <div class="relative min-h-screen w-full p-8 flex flex-col bg-cover justify-center bg-cover bg-no-repeat bg-center"
            style="background-image: url(/bg/3.jpg);">
            <div class="flex flex-col gap-8 text-white max-w-6xl mx-auto mt-12 p-6">
                <!-- 1 level -->
                <div class="lg:flex items-center gap-8 justify-center mx-auto">
                    <div class="bg-[#206038]  rounded-xl ring-4 ring-transparent hover:ring-[#ffcf03] p-4 flex flex-col items-center gap-2 mx-auto w-72">
                        <svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24" fill="none"
                            stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                            class="feather feather-award ">
                            <circle cx="12" cy="8" r="7"></circle>
                            <polyline points="8.21 13.89 7 23 12 20 17 23 15.79 13.88"></polyline>
                        </svg>
                        <span class="text-2xl md:text-4xl lg:text-5xl font-semibold">
                            <MiscCounter :max="220" />
                        </span>
                        <span class="text-xl font-semibold">Events Completed</span>
                    </div>
                </div>
                <!-- 2 level -->
                <div class="lg:flex items-center gap-8  justify-center mx-auto">
                    <div class="bg-[#206038] rounded-xl ring-4 ring-transparent  hover:ring-[#ffcf03] p-4 flex flex-col items-center gap-2 mx-auto w-72">

                        <svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24" fill="none"
                            stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                            class="feather feather-edit">
                            <path d="M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path>
                            <path d="M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z"></path>
                        </svg>
                        <span class="text-2xl md:text-4xl lg:text-5xl font-semibold">
                            <MiscCounter :max="480" />
                        </span>
                        <span class="text-xl font-semibold">Customer Reviews</span>
                    </div>
                    <div class="bg-[#206038]  rounded-xl ring-4 ring-transparent hover:ring-[#ffcf03] p-4 flex flex-col items-center gap-2 mx-auto w-72">
                        <svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24" fill="none"
                            stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                            class="feather feather-award">
                            <circle cx="12" cy="8" r="7"></circle>
                            <polyline points="8.21 13.89 7 23 12 20 17 23 15.79 13.88"></polyline>
                        </svg>
                        <span class="text-2xl md:text-4xl lg:text-5xl font-semibold">
                            <MiscCounter :max="220" />
                        </span>
                        <span class="text-xl font-semibold">Events Completed</span>
                    </div>
                </div>
                <!-- 3 level -->
                <div class="lg:flex items-center gap-8 justify-center mx-auto">

                    <div class="bg-[#206038] rounded-xl ring-4 ring-transparent hover:ring-[#ffcf03] p-4 flex flex-col items-center gap-2 mx-auto w-72">

                        <svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24" fill="none"
                            stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                            class="feather feather-edit">
                            <circle cx="12" cy="12" r="10"></circle>
                            <line x1="2" y1="12" x2="22" y2="12"></line>
                            <path
                                d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z">
                            </path>
                        </svg>
                        <span class="text-2xl md:text-4xl lg:text-5xl font-semibold">
                            <MiscCounter :max="200" />
                        </span>
                        <span class="text-xl font-semibold">Online Orders</span>
                    </div>
                    <div class="bg-[#206038]  rounded-xl ring-4 ring-transparent hover:ring-[#ffcf03] p-4 flex flex-col items-center gap-2 mx-auto w-72">

                        <svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24" fill="none"
                            stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                            class="feather feather-edit">
                            <path d="M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7"></path>
                            <path d="M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z"></path>
                        </svg>
                        <span class="text-2xl md:text-4xl lg:text-5xl font-semibold">
                            <MiscCounter :max="480" />
                        </span>
                        <span class="text-xl font-semibold">Customer Reviews</span>
                    </div>
                    <div class="bg-[#206038] rounded-xl ring-4 ring-transparent hover:ring-[#ffcf03] p-4 flex flex-col items-center gap-2 mx-auto w-72">
                        <svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24" fill="none"
                            stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                            class="feather feather-award">
                            <circle cx="12" cy="8" r="7"></circle>
                            <polyline points="8.21 13.89 7 23 12 20 17 23 15.79 13.88"></polyline>
                        </svg>
                        <span class="text-2xl md:text-4xl lg:text-5xl font-semibold">
                            <MiscCounter :max="220" />
                        </span>
                        <span class="text-xl font-semibold">Events Completed</span>
                    </div>
                </div>
            </div>
        </div>

        <div class="max-w-6xl mx-auto"><span class="font-bold text-xl md:text-3xl lg:text-4xl text-[#206038]">Customer
                Testimonials</span>
            <MiscCarosuel class="mt-5" :images="reviews.concat(reviews)"></MiscCarosuel>
        </div>
    </div>

</template>

<style scoped>
@keyframes bounceAlpha {
    0% {
        opacity: 1;
        transform: translateY(0px) scale(1);
    }

    25% {
        opacity: 0;
        transform: translateY(10px) scale(0.9);
    }

    26% {
        opacity: 0;
        transform: translateY(-10px) scale(0.9);
    }

    55% {
        opacity: 1;
        transform: translateY(0px) scale(1);
    }
}

.bounceAlpha {
    animation-name: bounceAlpha;
    animation-duration: 1.4s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
}

.feather-award:hover {
    stroke: #ffcf03; /* Change the stroke color to yellow when hovered */
}

.feather-edit:hover {
    stroke: #ffcf03; /* Change the stroke color to yellow when hovered */
}


</style>

<script setup lang="ts">
function scrollToMain() {
    window.scrollTo({ top: window.screen.height, left: 0, behavior: "smooth" })
}

const foods = [
    { name: "Dosa", image: "/dosa.jpg" },
    { name: "Idly", image: "/idli.jpg" },
    { name: "Idly", image: "/idli.jpg" },
    { name: "Parotta", image: "/parotta.jpg" },
    { name: "Parotta", image: "/parotta.jpg" },
    { name: "Idly", image: "/idli.jpg" },
    { name: "Parotta", image: "/parotta.jpg" },



]

const trymenu = [
    { name: "Dosa", image: "/dosa.jpg", ratings: 5 },
    { name: "Idly", image: "/idli.jpg", ratings: 5 },
    { name: "Idly", image: "/idli.jpg", ratings: 5 },
    { name: "Parotta", image: "/parotta.jpg", ratings: 5 },
    { name: "Parotta", image: "/parotta.jpg", ratings: 5 },

]
const menu = [
    { name: "Payasam", image: "/payasam/elaneer_payasam.jpg", link: "/payasam" },
    { name: "Idly", image: "/idli.jpg", link: "/idly" },
    { name: "Sweets", image: "/sweets/1.jpg", link: "/sweets" },
    { name: "Kootu", image: "/kootu/1.jpg", link: "/kootu" },
    { name: "Idly", image: "/idli.jpg", link: "/" },
    { name: "Parotta", image: "/parotta.jpg", link: "/" },
    { name: "Idly", image: "/idli.jpg", link: "/" },
    { name: "Parotta", image: "/parotta.jpg", link: "/" },

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