<template>
    <div class="w-full flex flex-col items-center">
        <div class="flex flex-row items-center space-x-4 max-w-6xl w-full overflow-x-hidden relative">
            <div class="relative inset-0 flex flex-row gap-8 justify-start transition-all duration-500 ease-in-out transform w-full md:w-[60rem]"
                :style="{ left: `-${current * 20}rem` }">
                <div v-for="item in images" :key="item"
                    class="p-[0.5rem] relative flex-shrink-0 flex flex-col items-start justify-start h-60 w-[19rem] px-2 py-4 shadow-xl rounded-xl">
                    <div class="text-lg font-bold">{{ item.name }}</div>
                    <MiscRating :score="item.ratings * 20" />
                    <div class="text-sm">{{ item.review }}</div>
                </div>
            </div>
            <button class="absolute left-0 inset-y-0 my-auto stroke-white fill-white stroke-2 transform rotate-180"
                @click="prev">
                <div class="rounded-full p-2 bg-black/70">
                    <svg width="24" height="24" viewBox="0 0 48 48" fill="white" stroke="white"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M24.2561 32.3144L23.5976 33.067C24.325 33.7035 25.4306 33.6298 26.067 32.9024L33.067 24.9024C33.6443 24.2426 33.6443 23.2574 33.067 22.5976L26.067 14.5976C25.4306 13.8703 24.325 13.7966 23.5976 14.433C22.8703 15.0694 22.7965 16.175 23.433 16.9024L27.8934 22H15.75C14.7835 22 14 22.7835 14 23.75C14 24.7165 14.7835 25.5 15.75 25.5H27.8934L23.433 30.5976C22.7965 31.325 22.8703 32.4306 23.5976 33.067L24.2561 32.3144Z"
                            stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                    </svg>
                </div>
            </button>
            <button class="absolute right-0 inset-y-0 my-auto stroke-white fill-white stroke-2" @click="next">
                <div class="rounded-full p-2 bg-black/70">
                    <svg width="24" height="24" viewBox="0 0 48 48" fill="white" stroke="white"
                        xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M24.2561 32.3144L23.5976 33.067C24.325 33.7035 25.4306 33.6298 26.067 32.9024L33.067 24.9024C33.6443 24.2426 33.6443 23.2574 33.067 22.5976L26.067 14.5976C25.4306 13.8703 24.325 13.7966 23.5976 14.433C22.8703 15.0694 22.7965 16.175 23.433 16.9024L27.8934 22H15.75C14.7835 22 14 22.7835 14 23.75C14 24.7165 14.7835 25.5 15.75 25.5H27.8934L23.433 30.5976C22.7965 31.325 22.8703 32.4306 23.5976 33.067L24.2561 32.3144Z"
                            stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                    </svg>
                </div>
            </button>
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
        current.value === images.length - 2 ? (current.value = 0) : next();
    }, 6000);
});

onBeforeUnmount(() => clearInterval(interval));

const next = () =>
    current.value === images.length - 2
        ? (current.value = 0)
        : current.value++;
const prev = () =>
    current.value === 0
        ? (current.value = images.length - 2)
        : current.value--;
</script>