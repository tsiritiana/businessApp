<template>
    <div class="bg-gray-900 py-24 sm:py-32">
        <div class="mx-auto max-w-6xl px-6 lg:px-8">
            <dl class="grid grid-cols-1 gap-x-8 gap-y-16 text-center lg:text-start lg:grid-cols-4">
                <div class="flex flex-col gap-5">
                    <h1 class="text-white font-bold">Pages</h1>
                    <section class="flex flex-col gap-5">
                        <p class="hover:text-white cursor:pointer">Home</p>
                        <p>Product</p>
                        <p>Pricing</p>
                        <p>About</p>
                        <p>Contact</p>
                    </section>
                </div>
                <div class="flex flex-col gap-5">
                    <h1 class="text-white font-bold">Tomothy</h1>
                    <section class="flex flex-col gap-5">
                        <p>Eleanor Edwards</p>
                        <p>Ted Robertson</p>
                        <p>Annette Russell</p>
                        <p>Jennie Mckinney</p>
                        <p>Gloria Richards</p>
                    </section>
                </div>
                <div class="flex flex-col gap-5">
                    <h1 class="text-white font-bold">Jane Black</h1>
                    <section class="flex flex-col gap-5">
                        <p>Philip Jones</p>
                        <p>Product</p>
                        <p>Colleen Russell</p>
                        <p>Marvin Hawkins</p>
                        <p>Bruce Simmmons</p>
                    </section>
                </div>

                <div class="flex flex-col gap-5 items-center">
                    <span class="max-w-md h-10 flex justify-start gap-2">
                        <MapPinIcon class="h-6 w-6 text-white" />
                        <p class="text-gray-400 text-sm">
                            7480 Mockingbird Hill
                        </p>
                    </span>
                    <span class="max-w-md h-10 flex justify-start gap-2">
                        <DevicePhoneMobileIcon class="h-6 w-6 text-white" />
                        <p class="text-gray-400 text-sm">
                            (239) 555-0108
                        </p>
                    </span>
                    <span class="max-w-md h-10 flex justify-start gap-2">
                        <img src="/img/twitter.png" alt="" srcset="">
                        <img src="/img/facebook.png" alt="" srcset="">
                        <img src="/img/linkdIn.png" alt="" srcset="">
                    </span>
                </div>
            </dl>
        </div>
    </div>
</template>

<script setup>
import { MapPinIcon, DevicePhoneMobileIcon, EnvelopeIcon } from '@heroicons/vue/24/outline'
</script>