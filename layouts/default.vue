<template>
    <div class="min-h-screen flex-col w-full tracking-wide font-montserrat">
        <LayoutHeader class="z-40" />
        <main class="grow-1 w-full relative z-20">
            <slot></slot>
        </main>
        <div class="fixed bottom-4 right-4 z-50">
            <button class="rounded-full w-16 h-16 bg-[#CBE7D8] border-green-800 border-4 rotate-180"
                @click="scollToTop">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
                    stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                    class="feather feather-chevron-right mx-auto">
                    <polyline points="18 6 12 12 6 6" class="bounceAlpha" style="animation-delay:0.2s;"></polyline>
                    <polyline points="18 17 12 23 6 17" class="bounceAlpha"></polyline>
                </svg>
            </button>
        </div>
        <LayoutPrefooter class="mt-12" />
        <LayoutFooter />
    </div>
</template>
<script setup lang="ts">
function scollToTop() {
    window.scrollTo({ top: 0, left: 0, behavior: "smooth" })
}
</script>