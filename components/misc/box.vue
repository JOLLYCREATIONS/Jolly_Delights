<template>
    <div><img class="rounded-xl w-full md:w-48" :src="image" />
        <div>{{ name }}</div>
    </div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
</script>