<script setup>
import { MapPinIcon, DevicePhoneMobileIcon, EnvelopeIcon } from '@heroicons/vue/24/outline'
import Map from './Map.vue'
</script>

<template>
    <div class="min-h-screen mx-auto flex flex-col gap-y-10 p-30 justify-center bg-white text-center text-gray-700">
        <div class="flex justify-center">
            <div class="text-center">
                <h1 class="flex flex-col justify-center items-center text-3xl gap-y-5">
                    <span>
                        Contact Us
                    </span>
                    <div class="w-[80px] h-[2.2px] rounded-full bg-blue-500">&nbsp;</div>
                </h1>
                <p class="max-w-sm mt-4 text-md text-gray-500 sm:text-xl/8">
                    Most calendars are designed for teams. Slate is designed for freelancers
                </p>
            </div>
        </div>
        <div class="flex flex-wrap justify-around">
            <div class="flex flex-col gap-3 sm:gap-6 text-center border border-gray-100 rounded-lg py-8 px-2 shadow-xl">
                <h1 class="text-xl font-semibold">
                    Contact Us
                </h1>
                <input type="text" placeholder="Your name"
                    class="px-4 py-2 text-gray-700 bg-gray-50 border border-gray-300 rounded-full focus:outline-none focus:ring-2 focus:ring-blue-400 focus:border-transparent mx-1 sm:mx-5 w-[300px] sm:w-80" />
                <input type="email" placeholder="Your Email"
                    class="px-4 py-2 text-gray-700 bg-gray-50 border border-gray-300 rounded-full focus:outline-none focus:ring-2 focus:ring-blue-400 focus:border-transparent mx-1 sm:mx-5 w-[300px] sm:w-80" />
                <textarea placeholder="Your Message"
                    class="px-4 py-2 h-32 text-gray-700 bg-gray-50 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-400 focus:border-transparent mx-1 sm:mx-5 w-[300px] sm:w-80" />
                <a href="#"
                    class="rounded-full bg-blue-500 font-semibold px-10 py-2.5 text-sm text-white hover:bg-indigo-500">
                    Send</a>
            </div>
            <div class="w-[700px]">
                <div class="flex flex-wrap justify-around gap-y-10 sm:gap-y-1 sm:gap-x-10 py-8 sm:py-1">
                    <span class="max-w-xs h-20 flex flex-col items-center justify-center gap-2">
                        <MapPinIcon class="h-10 w-10 text-blue-500" />
                        <p class="text-gray-700 text-sm">
                            4e arrondissement Paris
                        </p>
                    </span>
                    <span class="max-w-xs h-20 flex flex-col items-center justify-center gap-2">
                        <DevicePhoneMobileIcon class="h-8 w-8 text-blue-500" />
                        <p>(843) 555-0130</p>
                    </span>
                    <span class="max-w-xs h-20 flex flex-col items-center justify-center gap-2">
                        <EnvelopeIcon class="h-8 w-8 text-blue-500" />
                        <p>willie.jennings@example.com</p>
                    </span>
                </div>
                <Map class="hidden lg:block" />
                <span class="max-w-md hidden justify-start gap-2 p-2 lg:flex">
                    <img src="/img/twitter.png" alt="" class="size-7 bg-blue-500">
                    <img src="/img/facebook.png" alt="" class="size-7 bg-blue-500">
                    <img src="/img/linkdIn.png" alt="" class="size-7 bg-blue-500">
                </span>
            </div>
        </div>
    </div>
</template>
