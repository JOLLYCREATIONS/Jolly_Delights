<template>
    <header class="fixed top-0 left-0 w-full shadow-xl">
        <div class="bg-[#CBE7D8] w-full ">
            <div class="flex gap-12 items-center justify-between p-2 w-full mx-auto ">
                <a href="/" class="flex items-center gap-4 w-full">
                    <img src="/logo.png" class="w-12 h-12" alt="Jolly" />
                    <div class="w-full">
                        <div class="uppercase text-2xl text-[#206038] font-bold">Jolly Delights</div>
                        <div class="flex items-center">
                            <div class="text-md text-white font-bold bg-[#ffcf03] px-4 py-1 rounded">
                                Delights in every bite
                            </div>
                        </div>
                    </div>
                </a>
                <div class="flex items-center justify-end mr-4 gap-8 text-[#206038] grow-1 w-full">
                    <nav class="flex text-sm justify-end items-center gap-12 ">
                        <a class="font-bold transition duration-500 ease-in-out transform hover:scale-125 opacity-[0.75] hover:opacity-100 hover:text-[#467847]"
                            href="/">Home</a>
                        <a class="font-bold transition duration-500 ease-in-out transform hover:scale-125 opacity-[0.75] hover:opacity-100 hover:text-[#467847]"
                            href="/menu">Menu</a>
                        <a class="font-bold transition duration-500 ease-in-out transform hover:scale-125 opacity-[0.75] hover:opacity-100 hover:text-[#467847]"
                            href="/faq">FAQS</a>
                        <a class="font-bold transition duration-500 ease-in-out transform hover:scale-125 opacity-[0.75] hover:opacity-100 hover:text-[#467847]"
                            href="/getquote">Get Quotation</a>
                        <a class="font-bold transition duration-500 ease-in-out transform hover:scale-125 opacity-[0.75] hover:opacity-100 hover:text-[#467847]"
                            href="/aboutus">About Us</a>
                        <a class="font-bold transition duration-500 ease-in-out transform hover:scale-125 opacity-[0.75] hover:opacity-100 hover:text-[#467847] flex items-center gap-2 "
                            href="/contact">
                            <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24"
                                fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"
                                stroke-linejoin="round" class="feather feather-phone block shake">
                                <path
                                    d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z">
                                </path>
                            </svg><span>Contact Us</span></a>
                    </nav>
                </div>
            </div>
        </div>
    </header>
</template>
<style scoped>
.shake {
    animation: tilt-shaking 0.25s linear infinite;
}

@keyframes tilt-shaking {
    0% {
        transform: rotate(0deg);
    }

    25% {
        transform: rotate(5deg);
    }

    50% {
        transform: rotate(0eg);
    }

    75% {
        transform: rotate(-5deg);
    }

    100% {
        transform: rotate(0deg);
    }
}
</style>
