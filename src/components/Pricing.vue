<template>
    <div
        class="min-h-screen mx-auto flex flex-col gap-y-2 p-10 py-10 justify-center bg-gray-900 text-white text-center text-gray-700">
        <div class="flex justify-center">
            <div class="flex flex-col justify-between gap-5 text-center">
                <h1 class="flex flex-col justify-center items-center text-3xl gap-y-5">
                    <span>
                        Pricing
                    </span>
                    <div class="w-[80px] h-[2.2px] rounded-full bg-blue-500">&nbsp;</div>
                </h1>
                <p class="max-w-md text-md text-gray-300 sm:text-xl/8">
                    Most calendars are designed for teams. Slate is designed for freelancers
                </p>
            </div>
        </div>
        <div
            class="mx-auto mt-2 grid max-w-lg grid-cols-1 items-center sm:mt-2 gap-y-2 sm:gap-y-0 lg:max-w-4xl lg:grid-cols-3 lg:gap-x-20">
            <div v-for="(tier, tierIdx) in tiers" :key="tier.id"
                class="relative group block bg-white hover:bg-sky-600 transition duration-700 ease-in-out hover:cursor-pointer sm:mx-8 lg:mx-0 rounded-2xl p-8 ring-1 ring-gray-900/10 sm:p-8 sm:w-80">
                <h3 :id="tier.id" class="text-indigo-600 text-base/7 group-hover:text-white font-semibold">
                    {{ tier.name }}
                </h3>
                <p class="text-gray-600 text-xs text-base/7 group-hover:text-white">{{
                    tier.description }}
                </p>
                <p class="mt-4 flex justify-center items-baseline gap-x-2">
                    <span class="text-gray-900 group-hover:text-gray text-5xl font-extrabold tracking-tight">{{
                        tier.priceMonthly }}</span>
                    <span class="text-gray-500 text-base group-hover:text-white">/month</span>
                </p>
                <ul role="list" class="text-gray-600 mt-6 space-y-2 text-sm/6 sm:mt-6">
                    <li v-for="feature in tier.features" :key="feature" class="flex gap-x-3 group-hover:text-white">
                        <CheckIcon class="text-indigo-600 h-6 w-5 flex-none" aria-hidden="true" />
                        {{ feature }}
                    </li>
                </ul>
                <a :href="tier.href" :aria-describedby="tier.id"
                    class="text-indigo-600 group-hover:text-indigo-900 hover:bg-white ring-1 ring-inset ring-indigo-200 focus-visible:outline-indigo-600 mt-8 block rounded-md px-3.5 py-2.5 text-center text-sm font-semibold focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 sm:mt-10">
                    Order Now</a>
            </div>
        </div>
    </div>
</template>


<script setup>
import { CheckIcon } from '@heroicons/vue/20/solid'

const tiers = [
    {
        name: 'FREE',
        id: 'tier-hobby',
        href: '#',
        priceMonthly: '0 €',
        description: "Organize across all apps by hand",
        features: ['25 products', 'Up to 10,000 subscribers', 'Advanced analytics', '24-hour support response time'],
        featured: false,
    },
    {
        name: 'STANDARD',
        id: 'tier-enterprise',
        href: '#',
        priceMonthly: '10 €',
        description: 'Dedicated support and infrastructure for your company.',
        features: [
            'Unlimited products',
            'Unlimited subscribers',
            'Advanced analytics',
            'Dedicated support',
            'Marketing automations',
        ],
        featured: true,
    },
    {
        name: 'BUSINESS',
        id: 'tier-hobby',
        href: '#',
        priceMonthly: '99 €',
        description: "The perfect plan if you're just getting started with our product.",
        features: ['25 products', 'Up to 10,000 subscribers', 'Advanced analytics', '24-hour support response time'],
        featured: false,
    },
]
</script>