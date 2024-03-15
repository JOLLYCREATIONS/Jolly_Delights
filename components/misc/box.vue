<template>

    <div><img class="rounded-xl w-full lg:w-60 md:w-48 object-cover" :src="image" />
        <div class="md:text-lg lg:text-base truncate3  font-semibold ">{{ name }}</div>
        <button class="bg-green-800 transition ease-in-out hover:bg-yellow-600 block mt-2 p-2 w-full mx-auto rounded-md text-white"
            @click="() => emit(`added`)">Add To Cart</button>
    </div>
</template>
<script setup lang="ts">
const { name, image } = defineProps<{ name: string, image: string }>()
const emit = defineEmits<{ (e: "added"): void }>()
</script>