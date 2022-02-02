<template>
    <div class>
        <div class="pb-16 section-info lg:pb-0 lg:z-10 lg:relative">
            <div class="text-center mx-auto max-w-md px-4 sm:max-w-3xl sm:px-6 lg:px-8 lg:max-w-7xl">
                <p class="pt-5 text-3xl font-extrabold text-white tracking-tight sm:text-4xl">Testimonials</p>
            </div>
            <swiper :pagination="{ clickable: true }" :modules="modules" :slides-per-view="'auto'" :space-between="50" class="mySwiper grid grid-cols-1 lg:grid-cols-3">
                <swiper-slide v-for="post in blogPosts" :key="post.id" class="mb-16 cursor-pointer">
                    <div>
                        <div class="mt-12 lg:m-0 lg:col-span-2 lg:pl-8">
                            <div class="mx-auto max-w-md px-4 sm:max-w-2xl sm:px-6 lg:px-0 lg:py-20 lg:max-w-none">
                                <blockquote>
                                    <div>
                                        <svg class="h-12 w-12 text-white opacity-25" fill="currentColor" viewBox="0 0 32 32" aria-hidden="true">
                                            <path
                                                d="M9.352 4C4.456 7.456 1 13.12 1 19.36c0 5.088 3.072 8.064 6.624 8.064 3.36 0 5.856-2.688 5.856-5.856 0-3.168-2.208-5.472-5.088-5.472-.576 0-1.344.096-1.536.192.48-3.264 3.552-7.104 6.624-9.024L9.352 4zm16.512 0c-4.8 3.456-8.256 9.12-8.256 15.36 0 5.088 3.072 8.064 6.624 8.064 3.264 0 5.856-2.688 5.856-5.856 0-3.168-2.304-5.472-5.184-5.472-.576 0-1.248.096-1.44.192.48-3.264 3.456-7.104 6.528-9.024L25.864 4z"
                                            />
                                        </svg>
                                        <p
                                            class="mt-6 text-2xl font-medium text-white"
                                        >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed urna nulla vitae laoreet augue. Amet feugiat est integer dolor auctor adipiscing nunc urna, sit.</p>
                                    </div>
                                    <footer class="mt-10 flex">
                                        <div class="flex-shrink-0 inline-flex rounded-full border-2 border-white">
                                            <img
                                                class="h-12 w-12 rounded-full"
                                                src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
                                                alt
                                            />
                                        </div>
                                        <div class="ml-3">
                                            <p class="text-base font-medium text-white">Judith Black</p>
                                            <p class="text-base font-medium text-indigo-100">CEO at PureInsights</p>
                                        </div>
                                    </footer>
                                </blockquote>
                            </div>
                        </div>
                    </div>
                </swiper-slide>
            </swiper>
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
        icon: StarIcon,
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
        icon: StarIcon,
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
        icon: StarIcon,
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
        icon: StarIcon,
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
        icon: StarIcon,
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