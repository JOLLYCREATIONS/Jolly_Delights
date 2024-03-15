<template>
    <div class="flex items-center h-[25rem] relative max-w-7xl w-full mx-auto justify-center overflow-hidden"
        :style="{ perspective: `100rem`, }">
        <div v-for="item, i in data" :key="`${item.name}_${item.i}`"
            :class="`transition-all duration-500 ease-in-out absolute top-0 mx-auto w-24 lg:w-60 md:w-48 inset-x-0`"
            :style="{ marginTop: `3rem`, transform: `rotateY(${-10 * (item.i - current)}deg) translateX(${(Math.abs(item.i - current) >= 3) ? 1 : ((item.i - current) * 8)}rem) translateZ(${-1 * ((Math.abs(item.i - current) >= 3) ? 1 : Math.abs(item.i - current) * 15)}rem)`, transformStyle: `preserve-3d`, zIndex: -Math.abs(item.i - current) * 10, opacity: (Math.abs(item.i - current) < 3) ? 1 : 0 }">
            <img class="rounded-xl w-24 h-24 lg:w-60 md:w-48 lg:h-60 md:h-48 shadow-xl transition-all duration-500 ease-in-out"
                :src="item.image" />
        </div>
        <div :class="`md:text-lg lg:text-xl font-semibold relative top-[7rem]`">{{
            data[at].name }}
        </div>
    </div>
</template>
<script setup lang="ts">
const { items } = defineProps<{ items: { name: string, image: string }[] }>()

const data = ref(items.map((x, i) => ({ ...x, i })))

const mult = 360 / items.length

const current = ref(2)

const at = computed(() => current.value % items.length)

onMounted(() => {
    setInterval(() => {
        current.value += 1
        setTimeout(() => {
            data.value = [...data.value.slice(1), { name: data.value[0].name, image: data.value[0].image, i: (data.value.at(-1)?.i || 0) + 1 }]
        }, 500)
    }, 3000)
})

function rotate<T>(arr: T[], i: number): T[] {
    return [...arr.slice(i), ...arr.slice(0, i)]
}

</script>