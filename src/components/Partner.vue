<script setup>
const partners = [
    { id: 1, imageSrc: '/img/google.png' },
    { id: 2, imageSrc: '/img/amazon.png' },
    { id: 3, imageSrc: '/img/microsoft.png' },
    { id: 4, imageSrc: '/img/uber.png' },
]
const partners2 = [
    { id: 5, imageSrc: '/img/dropbox.png' },
    { id: 8, imageSrc: '/img/uber.png' },
    { id: 7, imageSrc: '/img/google.png' },
    { id: 6, imageSrc: '/img/amazon.png' },
]
</script>

<template>
    <div class="min-h-screen mx-auto flex flex-col gap-y-10 p-30 justify-center bg-white text-center text-gray-700">
        <div class="flex justify-center">
            <div class="text-center">
                <h1 class="flex flex-col justify-center items-center text-3xl gap-y-5">
                    <span>
                        Partners
                    </span>
                    <div class="w-[80px] h-[2.2px] rounded-full bg-blue-500">&nbsp;</div>
                </h1>
                <p class="max-w-sm mt-4 text-md text-gray-500 sm:text-xl/8">
                    Most calendars are designed for teams. Slate is designed for freelancers
                </p>
            </div>
        </div>
        <div class="flex justify-center">
            <div class="flex flex-wrap justify-center max-w-6xl">
                <img v-for="partner in partners" :key="partner.id" :src="partner.imageSrc" alt="" srcset=""
                    class="w-auto">
                <img v-for="partner in partners2" :key="partner.id" :src="partner.imageSrc" alt="" srcset=""
                    class="w-auto">
            </div>
        </div>
        <div class="flex justify-center">
            <a href="#"
                class="rounded-full bg-blue-500 font-semibold px-10 py-2.5 text-sm text-white hover:bg-indigo-500">
                Try For Free</a>
        </div>
    </div>
</template>