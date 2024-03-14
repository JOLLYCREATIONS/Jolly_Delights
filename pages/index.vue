<template>
    <div class="flex flex-col w-full items-center space-y-12">
        <div class="relative w-full h-screen flex flex-col justify-start">
            <video src="/promo.mp4" muted autoplay :controls="false" loop
                class="w-full h-screen object-cover  absolute z-10"></video>
            <div class="relative z-20 p-2 text-4xl lg:text-6xl text-white px-4 top-16 left-8 font-bold">
                Want to taste something
                Delicious?
            </div>
            <div class="relative z-20 p-2 text-xl lg:text-3xl text-white px-4 top-16 left-8">
                Here is the solution for all your
                party orders.
            </div>
            <div class="absolute z-20 w-full bottom-24 flex items-center justify-center gap-8 ">
                <button
                    class="p-6 uppercase bg-[#CBE7D8] transition ease-in-out hover:bg-yellow-600 text-black font-black text-sm rounded-md flex items-center gap-2">
                    <span>View more</span>
                </button>
                <button
                    class="p-6 uppercase bg-[#CBE7D8] transition ease-in-out hover:bg-yellow-600 text-black font-black text-sm rounded-md flex items-center gap-2">
                    <span>Call Us</span>
                </button>
            </div>
        </div>
        <div class="p-4 lg:p-8 w-full mx-auto flex flex-col gap-12">
            <div class="p-2 rounded-3xl bg-[#CBE7D8] text-black text-2xl ">
                <div class="p-2 w-full flex items-center gap-4">
                    <span
                        class="text-black font-bold text-xl md:text-3xl lg:text-4xl text-center underline mx-auto">Popular
                        Items</span>
                </div>
                <MiscCards :items="foods.concat(foods.concat(foods))" />
                <button
                    class="p-2 uppercase bg-yellow-600 text-black font-black text-xs rounded-lg flex items-center gap-2 mx-auto">

                    <span>Order Now</span>

                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none"
                        stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                        class="feather feather-chevron-right">
                        <polyline points="9 18 15 12 9 6"></polyline>
                    </svg>
                </button>
            </div>
            <div><span class="font-bold text-xl md:text-3xl lg:text-4xl text-[#206038]">Try Our New Arrivals</span>
                <div class="grid grid-cols-1 md:grid-cols-5 lg:grid-cols-10 items-center mt-5 gap-8">
                    <MiscBox v-for="food in foods.concat(foods.concat(foods.concat(foods.concat())))" :key="food.name"
                        :name="food.name" :image="food.image" />
                </div>
            </div>
            <div class="p-2 rounded-3xl bg-[#CBE7D8] text-black text-2xl ">
                <div class="p-4 w-full flex items-center gap-4">
                    <svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 24 24" fill="none"
                        stroke="currentColor" stroke-width="3" stroke-linecap="round" stroke-linejoin="round"
                        class="feather feather-search">
                        <circle cx="11" cy="11" r="8"></circle>
                        <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
                    </svg><span class="text-black font-bold text-xl md:text-3xl lg:text-4xl">Search By Category</span>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-10  md:grid-cols-5 items-center mt-5  gap-8">
                    <a v-for="food in menu.concat(menu.concat(menu.concat(menu.concat())))" :key="food.name" :href="food.link"><MiscCircle 
                        :name="food.name" :image="food.image" /></a>
                </div>
            </div>

        </div>
        <div class="mt-8 bg-[#206038] text-white w-full mt-12 p-4">
            <div class="lg:flex items-center gap-2 justify-between w-full">
                <div class="flex flex-col items-center gap-2 mx-auto">

                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
                        stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                        class="feather feather-users">
                        <path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"></path>
                        <circle cx="9" cy="7" r="4"></circle>
                        <path d="M23 21v-2a4 4 0 0 0-3-3.87"></path>
                        <path d="M16 3.13a4 4 0 0 1 0 7.75"></path>
                    </svg>
                    <span class="text-2xl md:text-4xl lg:text-5xl font-semibold">
                        <MiscCounter :max="987" />
                    </span>
                    <span class="text-xl font-semibold">Happy Customers</span>
                </div>
                <div class="flex flex-col items-center gap-2 mx-auto">

                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
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
                <div class="flex flex-col items-center gap-2 mx-auto">

                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
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
                <div class="flex flex-col items-center gap-2 mx-auto">

                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
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
                <div class="flex flex-col items-center gap-2 mx-auto">

                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
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
        <div><span class="font-bold text-xl md:text-3xl lg:text-4xl text-[#206038]">Customer Testimonials</span>
            <MiscCarosuel class="mt-5" :images="reviews.concat(reviews)"></MiscCarosuel>
        </div>
    </div>
</template>

<script setup lang="ts">
const foods = [
    { name: "Dosa", image: "/dosa.jpg"},
    { name: "Idly", image: "/idli.jpg"},
    { name: "Idly", image: "/idli.jpg"},
    { name: "Parotta", image: "/parotta.jpg"},
    { name: "Parotta", image: "/parotta.jpg"},


]
const menu = [
    { name: "Payasam", image: "/payasam/elaneer_payasam.jpg" ,link:"/payasam"},
    { name: "Idly", image: "/idli.jpg" ,link:"/idly"},
    { name: "Idly", image: "/idli.jpg" ,link:"/"} ,
    { name: "Parotta", image: "/parotta.jpg",link:"/"} ,
    { name: "Idly", image: "/idli.jpg",link:"/"},

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