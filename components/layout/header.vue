<template>
    <header class="fixed lg:relative top-0 left-0 w-full">
        <div class="bg-[#CBE7D8] w-full">
            <div class="flex gap-12 items-center justify-between p-2 max-w-[100rem] mx-auto">
                <div class="flex items-center gap-8 w-full">
                    <img src="/nitt_logo_min.webp" class="w-12 h-12" alt="Jolly" />
                    <div class="uppercase text-xl w-full">Jolly Delights</div>
                </div>
                <div class="flex items-center justify-between gap-8 grow-1 w-full">
                    <nav class="flex items-center gap-4">
                        <a href="/">Home</a>
                        <a href="/">Home</a>
                        <a href="/">Home</a>
                    </nav>
                    <ul class="flex items-center gap-4">
                        <a href="/login">Login</a>
                        <a href="/login">Login</a>
                        <MiscToggle :turnedOn="false" />
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>