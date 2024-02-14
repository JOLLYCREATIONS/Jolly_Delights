<template>
    <div><img class="rounded-xl w-full lg:w-72 md:w-60" :src="image" />
        <div class="text-lg md:text-xl lg:text-2xl font-semibold ">{{ name }}</div>
    </div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
</script>