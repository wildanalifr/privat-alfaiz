<template>
    <div class="relative bg-gray-50 py-16 sm:py-24 lg:py-32">
        <div class="relative">
            <div class="text-center mx-auto max-w-md px-4 sm:max-w-3xl sm:px-6 lg:px-8 lg:max-w-7xl">
                <p class="mt-2 text-3xl font-extrabold text-gray-900 tracking-tight sm:text-4xl">Try Out Terbaru</p>
            </div>
            <div class="mt-12 mx-auto max-w-md px-4 gap-8 sm:max-w-lg sm:px-6 lg:px-8 lg:max-w-7xl">
                <div>
                    <swiper :pagination="{ clickable: true }" :modules="modules" :slides-per-view="'auto'" :space-between="50" class="mySwiper grid grid-cols-1 lg:grid-cols-3">
                        <swiper-slide v-for="post in blogPosts" :key="post.id" class="mb-16 cursor-pointer">
                        <div class="shadow-md rounded-md overflow-hidden">
                                <div class="flex-shrink-0">
                                <img class="h-60 w-full object-cover" :src="post.imageUrl" alt />
                            </div>
                            <div class="flex-1 bg-white p-6 flex flex-col justify-between">
                                <div class="flex-1">
                                    <p class="text-sm font-medium text-red-600">
                                        <a class="hover:underline">{{ post.category.name }}</a>
                                    </p>
                                    <p  class="block mt-2">
                                        <p class="text-xl font-semibold text-gray-900">{{ post.title }}</p>
                                    </p>
                                </div>
                                <div class="mt-24 flex justify-between items-center">
                                    
                                    <div class="flex items-center">
                                        <component :is="post.icon" class="h-6 w-6" aria-hidden="true" v-if="post.status == 'Gratis'" />
                                        <p class="ml-2">{{post.status}}</p>
                                    </div>
                                    <div>
                                        <button type="button" class="inline-flex items-center p-3 border border-transparent text-base font-medium rounded-md text-red-700 bg-red-100 hover:bg-red-200 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
                                                        Detail Try Out
                                                    </button>
                                    </div>
                                   
                                </div>
                            </div>
                            </div>
                        </swiper-slide>
                    </swiper>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

import { StarIcon } from '@heroicons/vue/outline';

import { Swiper, SwiperSlide } from 'swiper/vue';
import { Pagination } from 'swiper'

// Import Swiper styles
import 'swiper/css';
import "swiper/css/pagination";

const blogPosts = [
    {
        id: 1,
        title: 'Boost your conversion rate',
        href: '#',
        date: 'Mar 16, 2020',
        datetime: '2020-03-16',
        category: { name: 'Article', href: '#' },
        imageUrl:
            'https://images.unsplash.com/photo-1496128858413-b36217c2ce36?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1679&q=80',

        status: 'Gratis',
        icon : StarIcon,
        readingLength: '6 min',
    },
    {
        id: 1,
        title: 'Boost your conversion rate',
        href: '#',
        date: 'Mar 16, 2020',
        datetime: '2020-03-16',
        category: { name: 'Article', href: '#' },
        imageUrl:
            'https://images.unsplash.com/photo-1496128858413-b36217c2ce36?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1679&q=80',

        status: 'Gratis',
        icon : StarIcon,
        readingLength: '6 min',
    },
    {
        id: 1,
        title: 'Boost your conversion rate',
        href: '#',
        date: 'Mar 16, 2020',
        datetime: '2020-03-16',
        category: { name: 'Article', href: '#' },
        imageUrl:
            'https://images.unsplash.com/photo-1496128858413-b36217c2ce36?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1679&q=80',

        status: 'Gratis',
        icon : StarIcon,
        readingLength: '6 min',
    },
    {
        id: 1,
        title: 'Boost your conversion rate',
        href: '#',
        date: 'Mar 16, 2020',
        datetime: '2020-03-16',
        category: { name: 'Article', href: '#' },
        imageUrl:
            'https://images.unsplash.com/photo-1496128858413-b36217c2ce36?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1679&q=80',
        status: 'Gratis',
        icon : StarIcon,
        readingLength: '6 min',
    },
    {
        id: 1,
        title: 'Boost your conversion rate',
        href: '#',
        date: 'Mar 16, 2020',
        datetime: '2020-03-16',
        category: { name: 'Article', href: '#' },
        imageUrl:
            'https://images.unsplash.com/photo-1496128858413-b36217c2ce36?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1679&q=80',
        status: 'Gratis',
        icon : StarIcon,
        readingLength: '6 min',
    },

]

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {


        return {
            modules: [Pagination],
            blogPosts,
        };
    },
};
</script>

