<template>
    <div class="flex flex-col items-center gap-3 "><img
            class="transition duration-500 ease-in-out transform hover:scale-110 ring-4 ring-transparent hover:shadow-2xl hover:ring-green-800 rounded-full w-full 2xl:w-44 2xl:h-44 xl:w-36 xl:h-36 w-30 h-30 lg:w-26 lg:h-26 md:w-32 md:h-32 " :src="image" />
        <div class="md:text-lg lg:text-xl text-center font-semibold ">{{ name }}</div>
    </div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
</script>
