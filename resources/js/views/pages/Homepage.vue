<script setup>
import Main from '@/views/layouts/Main'
import Icon from "@/views/components/icons/Icon.vue"
import Website from "@/views/components/Website.vue"
import Spinner from "@/views/components/icons/Spinner.vue";


const websites = [
    {
        name: 'DreamCarGiveawys',
        link: 'dream-car-giveways'
    },
    {
        name: 'RevComps',
        link: 'rev-comps'
    },
]


</script>

<template>
<Main>
    <div class="flex justify-center">

    <spinner v-if="true" class="w-10 h-10 "></spinner>
        <div role="list" class="divide-y divide-gray-100 w-1/2 bg-white  rounded">
            <!-- loop websites and pass the website as a prop to the website component -->
            <Website v-for="website in websites" :website="website"></Website>
        </div>
    </div>
</Main>
</template>
