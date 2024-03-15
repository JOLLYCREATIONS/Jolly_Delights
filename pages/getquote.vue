<template>
    <div class="relative w-full h-[50vh] flex flex-col justify-center">
        <img src="/header.webp" class="w-full h-[50vh] object-cover  absolute z-10 top-0">
    </div>

    <div class="p-8 grid grid-cols-4 gap-8">

        <div class="col-span-3 mt-4">
            <MiscAccordian title="Breakfast Menu">
                <div class="grid grid-cols-1 lg:grid-cols-6 items-center mt-5 gap-8">

                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image"
                        @added="() => addToCart(food)" />
                </div>
            </MiscAccordian>
            <MiscAccordian title="Lunch Menu">
                <div class="grid grid-cols-1 lg:grid-cols-6 items-center mt-5 gap-8">

                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image"
                        @added="() => addToCart(food)" />
                </div>
            </MiscAccordian>
            <MiscAccordian title="Dinner Menu">
                <div class="grid grid-cols-1 lg:grid-cols-6 items-center mt-5 gap-8">

                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image"
                        @added="() => addToCart(food)" />
                </div>
            </MiscAccordian>
            <MiscAccordian title="Dessert Menu">
                <div class="grid grid-cols-1 lg:grid-cols-6 items-center mt-5 gap-8">

                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image"
                        @added="() => addToCart(food)" />
                </div>
            </MiscAccordian>
            <MiscAccordian title="Snacks Menu">
                <div class="grid grid-cols-1 lg:grid-cols-6 items-center mt-5 gap-8">

                    <MiscBox v-for="food in foods" :key="food.name" :name="food.name" :image="food.image"
                        @added="() => addToCart(food)" />
                </div>
            </MiscAccordian>
        </div>
        <div>
            <div class="bg-[#C8E8D8] mt-4 p-4 flex flex-col text-semibold text-xl gap-6 ">
                <form class="grid grid-cols-2 gap-4">
                    <label for="date">Event Date </label>
                    <input class="p-2 rounded-md" id="date" type="Date" name="Event Date" required />

                    <label for="count">Head count </label>
                    <input class="p-2 rounded-md" id="count" type="text" name="Headcount" required />
                    <label for="type">Event Type </label>
                    <select class="p-2 rounded-md bg-white" name="type" id="type">
                        <option value="Wedding">Wedding</option>
                        <option value="Birthday">Birthday</option>
                        <option value="Grahapravesam">Grahapravesam</option>
                    </select>
                </form>
            </div>
            <div class="p-4 bg-[#206038]  text-white text-xl mt-4">
                <div class="text-white text-xl ">Order Review</div>
                <div class="flex flex-col gap-4 mt-4 items-stretch">
                    <div v-for="cartItem, i in cart" :key="i">
                        <div class="bg-white text-black rounded-md flex items-center p-2 gap 2 justify-between"><span>{{
                        cartItem.name }}</span>
                            <button @click="() => removeFromCart(i)">x</button>
                        </div>
                    </div>
                </div>
                <button class="bg-[#CBE7D8] gap 4 mt-4 px-4 py-2 mx-auto block rounded-md text-black"
                    @click="()=> cart=[]">Reset</button>
            </div>
            <div class="bg-[#C8E8D8] mt-4 p-4 flex flex-col text-semibold text-xl gap-6 ">
                <form class="grid grid-cols-2 gap-4">
                    <label for="name">Name</label>
                    <input class="p-2 rounded-md" id="name" type="text" minlength="3" name="name" required />

                    <label for="phone">Phone Number </label>
                    <input class="p-2 rounded-md" id="count" type="tel" name="phone" pattern="[0-9]{10}" required />
                    <button type="submit"
                        class="bg-[#ffcf03] gap 4 mt-4 px-4 py-2 mx-auto block rounded-md text-black">Submit</button>
                </form>
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
    { name: "Parotta", image: "/parotta.jpg" },
    { name: "Idly", image: "/idli.jpg" },
]

const cart = ref<{ name: string }[]>([])

function addToCart(item: { name: string }) {
    cart.value.push(item)

}
function removeFromCart(item: number) {
    cart.value.splice(item, 1)

}
</script>