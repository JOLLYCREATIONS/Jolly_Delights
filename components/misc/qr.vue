<template>
    <div><img class="rounded-xl" :src="image" />
        <div>{{ name }}</div>
    </div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
</script>