<template>
    <div :class="`p-2 flex flex-col items-stretch`">
        <div class="p-2 rounded-xl items-center flex justify-between bg-[#C8E8D8]">
            <div class="flex items-center gap-8">
                <div class="flex flex-col items-start gap-2">

                    <div class="text-base sm:text-xl lg:text-2xl font-semibold">{{ title }}
                    </div>
                </div>
            </div>
            <button @click="toggleDrop">
                <svg class="h-8 w-8 stroke-black stroke-2" xmlns="http://www.w3.org/2000/svg" fill="none"
                    viewBox="0 0 30 24" aria-hidden="true">
                    <path class="transition-all duration-500 transform ease-in-out" stroke-linecap="round"
                        stroke-linejoin="round" :d="editOpen
        ? `M 18 15 L 12 9 L 6 15` : `M 6 9 L 12 15 L 18 9`" />
                </svg></button>
        </div>
        <div
            :class="`${editOpen ? `max-h-[999rem]` : `max-h-[0rem]`} overflow-y-hidden transition-all duration-1000 ease-in-out bg-white flex flex-col space-y-4`">
            <div class="p-2"><slot></slot></div>
        </div>
    </div>

</template>
<script setup lang="ts">
const editOpen = ref(false)
const { title } = defineProps<{title: string}>()
const toggleDrop = () => editOpen.value = !editOpen.value
</script>