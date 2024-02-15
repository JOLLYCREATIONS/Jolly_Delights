<template>
    <div class="min-h-screen flex-col w-full tracking-wide font-montserrat">
        <LayoutHeader class="z-40" />
        <main class="grow-1 w-full relative z-20">
            <slot></slot>
        </main>
        <LayoutPrefooter class="mt-12" />
        <LayoutFooter />
    </div>
</template>