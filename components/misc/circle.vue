<template>
    <div class="flex flex-col items-center gap-3 "><img
            class="transition duration-500 ease-in-out transform hover:scale-110 ring-4 ring-transparent hover:shadow-2xl hover:ring-green-800 rounded-full w-full 2xl:w-40 2xl:h-40 xl:w-30 xl:h-30 w-24 h-24 lg:w-22 lg:h-22 md:w-26 md:h-26 " :src="image" />
        <div class="md:text-lg lg:text-xl text-center font-semibold ">{{ name }}</div>
    </div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
</script>
