<template>
    <span>{{ val }}</span>
</template>
<script setup lang="ts">
const { max } = defineProps<{ max: number }>()

const val = ref(0)

onMounted(() => {
    const stuff = setInterval(() => {
        if (val.value === max) clearInterval(stuff);
        else {
            val.value += 1;
        }
    }, 5)
})
</script>