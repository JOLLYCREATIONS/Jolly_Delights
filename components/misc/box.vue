<template>
    <div class="bg-[#CBE7D8] mx-auto mt-4 p-4 rounded-xl  object-cover transition duration-500 ease-in-out transform hover:scale-125">
    <div class="flex flex-col items-center md:w-48 sm:w-36 w-24 ">
        <div class="rounded-xl md:w-40 md:h-40 sm:w-32 sm:h-32  h-24 w-24 xl:w-40 xl:h-40">
        <img class="rounded-xl md:w-40 md:h-40 sm:w-32 sm:h-32 w-24 h-24 " :src="image" />
    </div>
        <div class="md:text-lg mt-4 lg:text-base truncate font-semibold  ">{{ name }}</div>
        <button
            class="rounded-xl  md:w-10 absolute bottom-0 left-0 sm:w-5  w-5 bg-green-800 transition ease-in-out hover:bg-[#ffcf03] hover:text-black block mt-2 p-1 w-full mx-auto rounded-md text-white text-xs sm:text-sm md:text-base"
            @click="() => emit(`added`)">A</button>
    </div>
</div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
const emit = defineEmits<{ (e: "added"): void }>()
</script>