<template>

    <div><img class="rounded-xl w-full mt-4 mb-4 lg:w-60 md:w-48 object-cover" :src="image" />
        <div class="md:text-lg lg:text-base truncate3  font-semibold ">{{ name }}</div>
    </div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
const emit = defineEmits<{ (e: "added"): void }>()
</script>