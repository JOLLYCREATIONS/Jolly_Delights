<template>
    <header class="fixed lg:relative top-0 left-0 w-full">
        <div class="bg-[#CBE7D8] w-full">
            <div class="flex gap-12 items-center justify-between p-2 max-w-[100rem] mx-auto">
                <div class="flex items-center gap-4 w-full">
                    <img src="/logo.png" class="w-12 h-12" alt="Jolly" />
                    <div class="uppercase text-2xl  w-full text-[#206038] font-bold">Jolly Delights</div>
                </div>
                <div class="flex items-center justify-between gap-8 text-[#206038] grow-1 w-full">
                    <nav class="flex text-xl items-center gap-4">
                        <a href="/">Home</a>
                        <a href="/">Menu</a>
                        <a href="/">FAQS</a>
                        <a href="/">About Us</a>

                    </nav>
                    <ul class="flex items-center gap-4">
                        <a href="/login">Contact Us</a>
                        <a href="/login">Login</a>
                        <MiscToggle :turnedOn="false" />
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>