<template>
    <div class="bg-green-100 p-2 shadow-xl w-72 flex flex-col gap-4"><img class="rounded-xl w-full" :src="image" />
        <a href="#" class="flex gap-2 p-2 mx-auto justify-center items-center bg-green-700 text-white rounded-md">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
                stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                class="feather feather-phone">
                <path
                    :d="icon">
                </path>
            </svg>
            <div>{{ name }}</div>
        </a>
</div></template>
<script setup lang="ts">
const { name, image, icon } = defineProps<{ name: string, image: string, icon: string }>()
</script>