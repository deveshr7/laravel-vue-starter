<script setup>

import Icon from "@/views/components/icons/Icon.vue";
import Button from "@/views/components/input/Button.vue";

//receive prop website from homepage
const props = defineProps({
    website: {
        type: Object,
    }
})

const website = props.website
</script>

<template>
    <div class="flex justify-between py-2 pr-2 leading-6 text-sky-500 whitespace-nowrap dark:text-sky-400 border-t border-slate-100 dark:border-slate-400/10 px-4 py-2 items-center">

        <div class="flex min-w-0 gap-x-4 items-center">
            <Icon name="star-o" class="text-gray-400 fa-regular cursor-pointer"/>
            <!-- create a link with vue router to a path -->
            <router-link :to="'site/' + website.link" class="text-sm font-semibold leading-6 text-gray-900">
                <div class="flex items-center space-x-4">
            <img class="h-8 w-8 flex-none rounded-full bg-gray-50" src="https://dreamcargiveaways.co.uk/favicon.ico" alt="">
            <div class="min-w-0 flex-auto ">
                <p class="text-sm font-semibold leading-6 text-gray-900">{{ website.name }}</p>
                <!--<p class="mt-1 truncate text-xs leading-5 text-gray-500">leslie.alexander@example.com</p>-->
            </div>
                </div>
                </router-link>
        </div>
        <div class="items-center">

            <a :href = "website.url">
            <button
                class="item-center middle none center flex justify-center rounded-lg p-3 font-sans text-xs font-bold uppercase text-white transition-all hover:shadow-lg focus:opacity-[0.85] focus:shadow-none active:opacity-[0.85] active:shadow-none disabled:pointer-events-none disabled:opacity-50 disabled:shadow-none"
                data-ripple-light="true"
            >
                <Icon name="external-link" class="text-gray-400 fa-regular !text-2xl rounded cursor-pointer"/>

            </button>
            </a>

            <!--
            <p class="text-sm leading-6 text-gray-900">Co-Founder / CEO</p>
            <p class="mt-1 text-xs leading-5 text-gray-500">Last seen <time datetime="2023-01-23T13:23Z">3h ago</time></p>
            -->
        </div>
    </div>
</template>
