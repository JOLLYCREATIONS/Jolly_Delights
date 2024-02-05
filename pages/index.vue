<template>
    <div class="flex flex-col w-full items-center space-y-12">
        <div class="relative w-full h-screen">
            <video src="/vid.mp4" muted autoplay :controls="false" loop
                class="w-full h-screen object-cover blur-sm absolute z-10"></video>
            <div class="relative z-20 text-2xl text-white">Hello Hello</div>
        </div>
        <div class="p-4 rounded-xl bg-[#] text-white w-full">HI</div>
    </div>
</template>