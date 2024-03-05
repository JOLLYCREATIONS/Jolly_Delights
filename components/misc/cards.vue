<template>
    <div class="flex items-center h-[20rem] relative max-w-7xl w-full mx-auto justify-center overflow-hidden"
        :style="{ perspective: `100rem`, }">
        <div v-for="item, i in items" :key="`${item.name}_${i}`"
            class="transition-all duration-500 ease-in-out absolute top-0 mx-auto lg:w-60 md:w-48 inset-x-0"
            :style="{ marginTop: `3rem`, transform: `rotateY(${30 * (i - current)}deg) translateX(${((i - current) <= -3 || (i - current) >= 3) ? 0 : ((i - current) * Math.abs(i - current) * 10)}rem)`, transformStyle: `preserve-3d`, zIndex: -Math.abs(i - current), opacity: Math.abs(i - current) < 3 ? 1 : 0 }">
            <img class="rounded-xl w-full lg:w-60 md:w-48 shadow-xl transition-all duration-500 ease-in-out"
                :src="item.image" />
        </div>
        <div :class="`md:text-lg lg:text-xl font-semibold relative top-[7rem]`">{{
            items[current].name }}
        </div>
    </div>
</template>
<script setup lang="ts">
const { items } = defineProps<{ items: { name: string, image: string }[] }>()

const current = ref(2)

onMounted(() => {
    setInterval(() => {
        current.value = current.value === items.length - 3 ? 2 : current.value + 1
    }, 1000)
})

function rotate<T>(arr: T[], i: number): T[] {
    return [...arr.slice(i), ...arr.slice(0, i)]
}

</script>