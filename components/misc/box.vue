<template>
    <div
        class="bg-[#CBE7D8] mx-auto mt-4 p-2 py-4 rounded-xl hover:border-green-800 hover:border-4 object-cover transition duration-500 ease-in-out transform hover:scale-105">
        <div class="flex flex-col items-center md:w-48 sm:w-36 w-24 ">
            <div class="rounded-xl md:w-44 md:h-44 sm:w-32 sm:h-32  h-24 w-24">
                <img class="rounded-xl md:w-44 md:h-44 sm:w-32 sm:h-32 w-24 h-24 " :src="image" />
            </div>
            <div class="md:text-lg mt-2 lg:text-base truncate font-semibold  ">{{ name }}</div>
            <MiscRating :score="(ratings ?? 5) * 20" />
            <button
                class="rounded-xl  md:w-20 sm:w-20 hover:w-full w-20 bg-green-800 transition ease-in-out  block mt-2 p-1 w-full mx-auto rounded-md text-white text-xs sm:text-sm md:text-base"
                @click="() => emit(`added`)">A</button>
        </div>
    </div>
</template>
<script setup lang="ts">
const { name, image, ratings } = defineProps<{ name: string, image: string, ratings?: number }>()
const emit = defineEmits<{ (e: "added"): void }>()
</script>