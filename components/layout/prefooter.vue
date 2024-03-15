<template>
    <div class="w-full bg-green-800 text-white bg-cover bg-fixed bg-center" style="background-image:url(/header.webp)">
        <div class="lg:flex items-center justify-center gap-12 w-full bg-black/40 py-8">
            <div class="text-2xl md:text-4xl lg:text-5xl font-black text-center max-w-xl">
                Are you ready to order with the best deals?
            </div>
            <button class="p-2 uppercase bg-[#ffcf03] text-black font-black text-xs rounded-lg flex items-center gap-2">

                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
                    stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                    class="feather feather-shopping-cart">
                    <circle cx="9" cy="21" r="1"></circle>
                    <circle cx="20" cy="21" r="1"></circle>
                    <path d="M1 1h4l2.68 13.39a2 2 0 0 0 2 1.61h9.72a2 2 0 0 0 2-1.61L23 6H6"></path>
                </svg>
                <span>Proceed To Order</span>

                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none"
                    stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                    class="feather feather-chevron-right">
                    <polyline points="9 18 15 12 9 6"></polyline>
                </svg>
            </button>
        </div>
    </div>
</template>