<template>
    <div class="flex flex-col w-full items-center space-y-12">
        <div class="relative w-full h-screen flex flex-col justify-center">
            <video src="/vid.mp4" muted autoplay :controls="false" loop
                class="w-full h-screen object-cover  absolute z-10"></video>
            <div class="relative z-20  text-6xl text-white px-4">Want to taste something Delicious</div>
        </div>
        <div class="max-w-7xl mx-auto flex flex-col gap-12">
            <div class="p-4 rounded-xl bg-[#CBE7D8] text-white w-full">Popular Items</div>
            <div>
                <div class="p-4 rounded-xl bg-[#fffff] text-[#206038] font-bold text-6xl w-full">Try Our New Arrivals</div>
                <div class="grid grid-cols-1 lg:grid-cols-2 lg:grid-cols-3 lg:grid-cols-4 items-center rounded-2xl gap-8">
                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
                </div>
            </div>
            <div class="p-4 rounded-xl bg-[#CBE7D8] text-black text-2xl ">
                <div class="p-4 rounded-xl bg-[#fffff] text-black font-bold text-6xl w-full">Search By Food</div>

                <div class="grid grid-cols-1 lg:grid-cols-5  md:grid-cols-4 items-center mt-5  gap-8">
                    <MiscCircle v-for="food in menu" :key="food.name" :name="food.name" :image="food.image" />
                    <MiscCircle v-for="food in menu" :key="food.name" :name="food.name" :image="food.image" />
                </div>
            </div>
            <MiscCarosuel :images="events"></MiscCarosuel>
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
const events=[
{
      title: {
        en: "An awareness event for women and children - Chennai Central Railway Station - presence of DIG Balakrishnan and Judge Jayanthi and police officers.",
        ta:
          "சென்னை சென்ட்ரல் ரயில்வே நிலையத்தில் பெண்களுக்கும் குழந்தைகளுக்குமான விழிப்புணர்வு நிகழ்வு டிஐஜி பாலகிருஷ்ணன் மற்றும் ஜட்ஜ் ஜெயந்தி மற்றும் காவல்துறையினர்கள் முன்னிலையில் சிறப்பாக நடைபெற்றது",
      },
      image: "/idli.jpg"
    },
]
</script>