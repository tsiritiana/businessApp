<template>
    <div class="h-screen mx-auto flex flex-col gap-y-20 p-30 justify-center bg-white text-center text-gray-700">
        <div class="flex flex-wrap justify-center gap-x-20">
            <span>
                <img src="/img/newsletter.png" alt="" srcset="" class="w-96">
            </span>
            <div class="sm:text-start">
                <p class="text-sm font-bold">At your fingertips</p>
                <h1 class="text-3xl mt-4">
                    Lightning fast prototyping
                </h1>
                <span class="max-w-sm">
                    <p class="mt-8 text-xs font-bold">
                        Subscribe to our Newsletter
                    </p>
                    <p class="text-xs text-gray-500">Available exclusivery on Figmaland</p>
                </span>
                <div class="mt-10 flex flex-wrap justify-center gap-3 sm:justify-start sm:gap-x-6 ">
                    <input type="email" placeholder="Your Email"
                        class="px-4 py-2 text-gray-700 bg-gray-50 border border-gray-300 rounded-full focus:outline-none focus:ring-2 focus:ring-blue-400 focus:border-transparent w-80" />
                    <a href="#"
                        class="rounded-full bg-blue-500 font-semibold px-10 py-2.5 text-sm text-white hover:bg-indigo-500">
                        Subscribe</a>
                </div>
            </div>
        </div>
    </div>
</template>