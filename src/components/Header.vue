<script setup lang="ts">
import { ref } from 'vue'
import { Dialog, DialogPanel } from '@headlessui/vue'
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/outline'

const navigation = [
    { name: 'Home', href: '#' },
    { name: 'Product', href: '#' },
    { name: 'Pricing', href: '#' },
    { name: 'About', href: '#' },
    { name: 'Contact', href: '#' },
]
const mobileMenuOpen = ref(false)
</script>

<template>
    <div class="w-screen h-screen bg-cover bg-[url('/img/bgImage.jpg')]">
        <header class="absolute inset-x-0 top-0 z-50">
            <nav class="p-12 lg:px-20" aria-label="Global">
                <div class="flex justify-around">
                    <div class="hidden lg:flex lg:gap-x-8">
                        <a v-for="item in navigation" :key="item.name" :href="item.href"
                            class="text-sm text-gray-300 font-semibold pt-1 hover:text-white">
                            {{ item.name }}
                        </a>
                        <a href="#" class="">
                            <span class="sr-only">Logo figmaLand</span>
                            <img class="h-7 w-auto" src="/img/logoFigma.png" alt="Logo FigmaLand" />
                        </a>
                    </div>
                    <div class="hidden lg:flex lg:justify-center lg:gap-x-4">
                        <a href="#">
                            <img src="/img/twitter.png" alt="" class="w-auto h-8">
                        </a>
                        <a href="#">
                            <img src="/img/facebook.png" alt="" class="w-auto h-8">
                        </a>
                        <a href="#">
                            <img src="/img/linkdIn.png" alt="" class="w-auto h-8">
                        </a>
                    </div>
                </div>
                <div class="flex justify-between lg:hidden">
                    <a href="#" class="">
                        <span class="sr-only">Logo figmaLand</span>
                        <img class="h-7 w-auto" src="/img/logoFigma.png" alt="Logo FigmaLand" />
                    </a>
                    <button type="button"
                        class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-white"
                        @click="mobileMenuOpen = true">
                        <span class="sr-only">Open main menu</span>
                        <Bars3Icon class="size-6" aria-hidden="true" />
                    </button>
                </div>
            </nav>
            <Dialog class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
                <div class="fixed inset-0 z-50" />
                <DialogPanel
                    class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-gray-600 px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
                    <div class="flex items-center justify-between">
                        <a href="#" class="">
                            <span class="sr-only">Logo figmaLand</span>
                            <img class="h-7 w-auto" src="/img/logoFigma.png" alt="Logo FigmaLand" />
                        </a>
                        <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700"
                            @click="mobileMenuOpen = false">
                            <span class="sr-only">Close menu</span>
                            <XMarkIcon class="size-6" aria-hidden="true" />
                        </button>
                    </div>
                    <div class="mt-6 flow-root">
                        <div class="-my-6 divide-y divide-gray-500/10">
                            <div class="space-y-2 py-6">
                                <a v-for="item in navigation" :key="item.name" :href="item.href"
                                    class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-white hover:bg-gray-50">{{
                                        item.name }}</a>
                            </div>
                        </div>
                    </div>
                </DialogPanel>
            </Dialog>
        </header>

        <div class="relative isolate px-6 pt-28 lg:px-8">
            <div class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80"
                aria-hidden="true">
                <div class="relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]"
                    style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
            </div>
            <div class="mx-auto max-w-2xl py-30 sm:py-48 lg:py-20">
                <div class="text-center">
                    <h1 class="text-balance text-white text-4xl font-bold tracking-tight sm:text-6xl">
                        The best products start with Figma
                    </h1>
                    <p class="mt-8 text-gray-300 text-lg font-medium sm:text-xl/8">
                        Most calendars are designed for teams. Slate is designed for freelancers
                    </p>
                    <div class="mt-20 flex items-center justify-center gap-x-6">
                        <a href="#"
                            class="rounded-full bg-blue-500 px-10 py-2.5 text-sm text-white hover:bg-indigo-500">
                            Try For Free</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>