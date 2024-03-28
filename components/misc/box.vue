<template>
    <div class="flex flex-col items-center md:w-48 sm:w-36 w-24 ">
        <div class="rounded-xl md:w-40 md:h-40 sm:w-32 sm:h-32  lg:w-20 lg:h-20 h-24 w-24 xl:w-40 xl:h-40">
        <img class="rounded-xl md:w-40 md:h-40 sm:w-32 sm:h-32 w-24 h-24 lg:w-20 lg:h-20 object-cover transition duration-500 ease-in-out transform hover:scale-125" :src="image" />
    </div>
        <div class="md:text-lg mt-4 lg:text-base truncate font-semibold ">{{ name }}</div>
        <button
            class="rounded-xl md:w-40 sm:w-32  w-24 bg-green-800 transition ease-in-out hover:bg-[#ffcf03] block mt-2 p-2 w-full mx-auto rounded-md text-white text-xs sm:text-sm md:text-base"
            @click="() => emit(`added`)">Add To Cart</button>
    </div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
const emit = defineEmits<{ (e: "added"): void }>()
</script>