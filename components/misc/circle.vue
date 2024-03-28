<template>
    <div class="flex flex-col items-center gap-3"><img
            class="rounded-full w-full xl:w-28 xl:h-28 w-16 h-16 lg:w-20 lg:h-20 md:w-32 md:h-32" :src="image" />
        <div class="md:text-lg lg:text-xl text-center font-semibold ">{{ name }}</div>
    </div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
</script>
