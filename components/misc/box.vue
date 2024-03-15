<template>
    <div class="md:w-48 sm:w-36 w-24">
        <div class="rounded-xl md:w-48 sm:w-36 w-24">
        <img class="rounded-xl md:w-48 sm:w-36 w-24 object-cover transition duration-500 ease-in-out transform hover:scale-125" :src="image" />
    </div>
        <div class="md:text-lg lg:text-base truncate font-semibold ">{{ name }}</div>
        <button
            class="bg-green-800 transition ease-in-out hover:bg-[#ffcf03] block mt-2 p-2 w-full mx-auto rounded-md text-white text-xs sm:text-sm md:text-base"
            @click="() => emit(`added`)">Add To Cart</button>
    </div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
const emit = defineEmits<{ (e: "added"): void }>()
</script>