<template>
    <div><img class="rounded-xl w-full lg:w-60 md:w-48 object-cover" :src="image" />
        <div class="md:text-lg lg:text-xl font-semibold ">{{ name }}</div>
    </div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
</script>