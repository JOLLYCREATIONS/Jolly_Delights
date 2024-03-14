<template>
    <div class="relative w-full h-[50vh] flex flex-col justify-center">
        <img src="/header.webp" class="w-full h-[50vh] object-cover  absolute z-10 top-0">
    </div>
    <div class="grid grid-cols-3">

        <div class="col-span-2 mt-4">
            <MiscAccordian title="Breakfast Menu">
                <div class="grid grid-cols-1 lg:grid-cols-6 items-center mt-5 gap-8">

                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
                </div>
            </MiscAccordian>
            <MiscAccordian title="Lunch Menu">
                <div class="grid grid-cols-1 lg:grid-cols-6 items-center mt-5 gap-8">

                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
                </div>
            </MiscAccordian>
            <MiscAccordian title="Dinner Menu">
                <div class="grid grid-cols-1 lg:grid-cols-6 items-center mt-5 gap-8">

                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
                </div>
            </MiscAccordian>
            <MiscAccordian title="Dessert Menu">
                <div class="grid grid-cols-1 lg:grid-cols-6 items-center mt-5 gap-8">

                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
                </div>
            </MiscAccordian>
            <MiscAccordian title="Snacks Menu">
                <div class="grid grid-cols-1 lg:grid-cols-6 items-center mt-5 gap-8">

                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image" />
                </div>
            </MiscAccordian>
        </div>
        <div class="bg-[#C8E8D8] mt-4">
            <label>Event Date
           <input type="Date" name="Event Date" />
        </label>
            <label>Head count
                <input type="text" name="Headcount"/>
            </label>
            <label>Event Type
                <select name="type" id="type">
                    <option value="Wedding">Wedding</option>
                    <option value="Wedding">Birthday</option>
                    <option value="Wedding">Grahapravesam</option>
                </select>
            </label>
        </div>
    </div>
</template>
<script setup lang="ts">
const foods = [
    { name: "Dosa", image: "/dosa.jpg" },
    { name: "Idly", image: "/idli.jpg" },
    { name: "Idly", image: "/idli.jpg" },
    { name: "Parotta", image: "/parotta.jpg" },
    { name: "Parotta", image: "/parotta.jpg" },
    { name: "Idly", image: "/idli.jpg" },
]
</script>