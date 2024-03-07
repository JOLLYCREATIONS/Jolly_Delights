<template>
    <div class="relative w-full h-[50vh] flex flex-col justify-center">
        <img src="/header.webp" class="w-full h-[50vh] object-cover  absolute z-10 top-0">
    </div>
    <div class="p-4 mt-16 max-w-7xl xl:max-w-[90 rem] mx-auto rounded-xl items-center  bg-[#CBE7D8] text-black text-2xl flex flex-col lg:flex-row gap-2 lg:justify-between">
    <div  class="flex flex-col items-start gap-4 ">
        <h1 class="text-center mt-2 font-bold">Our Story</h1>
        <p class="mt-4 ">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean efficitur finibus tempor. Quisque
            porta commodo sodales. Cras cursus vel dui non lacinia. Vestibulum ut vulputate dolor. Orci varius natoque penatibus et magnis
            dis parturient montes, nascetur ridiculus mus. Maecenas felis augue, placerat in erat sit amet, malesuada
            venenatis odio. Sed euismod luctus ornare. Maecenas mollis in lectus id ornare. Nunc quis eleifend elit, sed
            mattis nulla. Suspendisse malesuada neque vitae nulla rhoncus pharetra. Praesent auctor condimentum vestibulum.
        </p>
    </div>
        <img src="/idli.jpg" class="p-8">
    </div>
    <div class="p-4 mt-16 max-w-7xl xl:max-w-[90 rem] mx-auto rounded-xl items-center  bg-[#CBE7D8] text-black text-2xl flex flex-col lg:flex-row gap-2 lg:justify-between">
    <div  class="flex flex-col items-start gap-4 ">
        <h1 class="text-center mt-2 font-bold">Our Story</h1>
        <p class="mt-4 ">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean efficitur finibus tempor. Quisque
            porta commodo sodales. Cras cursus vel dui non lacinia. Vestibulum ut vulputate dolor. Orci varius natoque penatibus et magnis
            dis parturient montes, nascetur ridiculus mus. Maecenas felis augue, placerat in erat sit amet, malesuada
            venenatis odio. Sed euismod luctus ornare. Maecenas mollis in lectus id ornare. Nunc quis eleifend elit, sed
            mattis nulla. Suspendisse malesuada neque vitae nulla rhoncus pharetra. Praesent auctor condimentum vestibulum.
        </p>
    </div>
        <img src="/idli.jpg" class="p-8">
    </div>
    <div class="mt-16 mx-auto max-w-7xl xl:max-w-[90 rem] flex flex-col lg:flex-row gap-2 lg:justify-between items-center rounded-2xl  mx-auto gap-8">
            <MiscBox v-for="food in foods.concat()" :key="food.name" :name="food.name" :image="food.image" class="mx-auto" />
        </div>

</template>

<script setup lang="ts">
const foods = [
    { name: "Dosa", image: "/dosa.jpg" },
    { name: "Idly", image: "/idli.jpg" },
    { name: "Idly", image: "/idli.jpg" },
]
</script>