<template>
    <div class="w-full flex flex-col items-center gap-4">
        <div class="flex flex-row items-center md:w-[58rem] w-full overflow-x-hidden relative p-[1rem]">
            <div class="relative inset-0 flex flex-row gap-[1rem] justify-start transition-all duration-500 ease-in-out transform w-full md:w-[56rem]"
                :style="{ transform: `translateX(-${current * 19}rem)` }">
                <div v-for="item in images" :key="item"
                    class="p-[0.5rem] relative flex-shrink-0 flex flex-col items-start justify-start h-60 w-[18rem] px-2 py-4 shadow-xl rounded-xl">
                    <div class="text-lg font-bold">{{ item.name }}</div>
                    <MiscRating :score="item.ratings * 20" />
                    <div class="text-sm">{{ item.review }}</div>
                </div>
            </div>
        </div>
        <div class="flex items-center gap-2">
            <button v-for="item, i in images.slice(0, images.length - 2)" :key="item"
                :class="`w-8 h-8 rounded-full ${Math.abs(current - (i)) <= 1 ? `bg-[#ffcf03]` : `bg-green-900`}`"
                @click="() => current = i"></button>
        </div>

    </div>
</template>
<script setup>
const languageSettings = { useTamil: true };

const { images } = defineProps(["images"]);

const current = ref(0);

const img = computed(() => {
    const i = [];
    let m = 0;
    for (let n in images) {
        i.push(images.at(current.value + m));
        m++;
    }
    return i;
});
let interval;
onMounted(() => {
    interval = setInterval(() => {
        next();
    }, 6000);
});

onBeforeUnmount(() => clearInterval(interval));

const next = () =>
    current.value >= images.length - 3
        ? (current.value = 0)
        : current.value++;
const prev = () =>
    current.value === 0
        ? (current.value = images.length - 3)
        : current.value--;
</script>