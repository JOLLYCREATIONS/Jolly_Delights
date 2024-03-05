<template>
    <div class="flex flex-col items-center gap-3"><img class="rounded-full w-full xl:w-40 h-40 lg:w-32  lg:h-32 md:w-32 md:h-32" :src="image" />
        <div class="md:text-lg lg:text-xl text-center font-semibold ">{{ name }}</div>
    </div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
</script>