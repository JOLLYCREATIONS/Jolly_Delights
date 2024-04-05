<template>
    <div
        class="overflow-hidden bg-[#CBE7D8] mx-auto mt-4 rounded-xl ring-4 ring-transparent hover:ring-green-800 transition duration-500 ease-in-out transform hover:scale-105">
        <div class="flex flex-col items-center xl:w-48 lg:w-36 w-24">
            <div class="flex flex-col w-full gap-2 px-2 py-4">
                <div class="rounded-xl xl:w-44 xl:h-44 lg:w-32 lg:h-32  h-24 w-24">
                    <img class="rounded-xl xl:w-44 xl:h-44 lg:w-32 lg:h-32 w-24 h-24 " :src="image" />
                </div>
                <div class="md:text-lg mt-2 lg:text-base truncate font-semibold  ">{{ name }}</div>
                <MiscRating :score="(ratings ?? 5) * 20" />
            </div>
            <button
                class="w-full bg-green-800 transition ease-in-out block  w-full mx-auto text-white text-xs sm:text-sm md:text-base"
                @click="() => emit(`added`)">
                <MiscWeirdbutton>Add To Menu</MiscWeirdbutton>
            </button>
        </div>
    </div>
</template>
<script setup lang="ts">
const { name, image, ratings } = defineProps<{ name: string, image: string, ratings?: number }>()
const emit = defineEmits<{ (e: "added"): void }>()
</script>