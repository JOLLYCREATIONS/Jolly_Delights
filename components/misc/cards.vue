<template>
    <div class="flex items-center h-[15rem] relative w-[45rem] mx-auto justify-center overflow-hidden">
        <div v-for="item, i in items" :key="`${item.name}_${i}`">
            <div class="transition-all duration-500 ease-in-out absolute top-0 mx-auto w-60 inset-x-0"
                :style="{ transform: `rotateY(${30 * (i - current)}deg) translateX(${(i - current) * 15}rem) perspective(50rem)`, zIndex: 990 - Math.abs(i - current), opacity: Math.abs(i - current) < 3 ? 1 : 0 }">
                <img class="rounded-xl w-full lg:w-60 md:w-48 shadow-xl transition-all duration-500 ease-in-out"
                    :src="item.image" />

            </div>
            <div :class="`md:text-lg lg:text-xl font-semibold relative top-[6rem] ${i === 2 ? `block` : `hidden`}`">{{
                items[current].name }}</div>
        </div>
    </div>
</template>
<script setup lang="ts">
const { items } = defineProps<{ items: { name: string, image: string }[] }>()

const current = ref(1)

onMounted(() => {
    setInterval(() => {
        current.value = current.value === items.length - 2 ? 1 : current.value + 1
    }, 1000)
})

function rotate<T>(arr: T[], i: number): T[] {
    return [...arr.slice(i), ...arr.slice(0, i)]
}

</script>