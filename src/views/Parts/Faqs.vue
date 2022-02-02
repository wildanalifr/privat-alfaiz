<!-- This example requires Tailwind CSS v2.0+ -->
<template>
    <div class="mx-auto py-12 px-4 sm:py-16 bg-gray-50">
        <div class="text-center mx-auto max-w-md px-4 sm:max-w-5xl sm:px-6 lg:px-8 divide-y-2 divide-gray-200">
            <h2 class="text-center mb-10 text-xl md:text-3xl font-bold text-gray-900 tracking-wide">Pertanyaan Seputar Al Faiz</h2>
            <dl class="mt-6 space-y-6 divide-y divide-gray-200">
                <Disclosure as="div" v-for="faq in faqs" :key="faq.question" class="pt-6" v-slot="{ open }">
                    <dt class="text-lg">
                        <DisclosureButton class="text-left w-full flex justify-between items-start text-gray-400">
                            <span class="font-medium text-gray-900">{{ faq.question }}</span>
                            <span class="ml-6 h-7 flex items-center">
                                <ChevronDownIcon :class="[open ? '-rotate-180' : 'rotate-0', 'h-6 w-6 transform']" aria-hidden="true" />
                            </span>
                        </DisclosureButton>
                    </dt>
                    <DisclosurePanel as="dd" class="mt-3 pr-12">
                        <p class="text-base text-gray-500">{{ faq.answer }}</p>
                    </DisclosurePanel>
                </Disclosure>
            </dl>
        </div>
    </div>
</template>

<script>
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import { ChevronDownIcon } from '@heroicons/vue/outline'

const faqs = [
    {
        question: "What's the best thing about Switzerland?",
        answer:
            "I don't know, but the flag is a big plus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
    },
    {
        question: "What's the best thing about Switzerland?",
        answer:
            "I don't know, but the flag is a big plus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
    },
    {
        question: "What's the best thing about Switzerland?",
        answer:
            "I don't know, but the flag is a big plus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
    },
    {
        question: "What's the best thing about Switzerland?",
        answer:
            "I don't know, but the flag is a big plus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
    },
    {
        question: "What's the best thing about Switzerland?",
        answer:
            "I don't know, but the flag is a big plus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
    },
]

export default {
    components: {
        Disclosure,
        DisclosureButton,
        DisclosurePanel,
        ChevronDownIcon,
    },
    setup() {
        return {
            faqs,
        }
    },
}
</script>