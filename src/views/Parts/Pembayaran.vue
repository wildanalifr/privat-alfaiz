<!-- This example requires Tailwind CSS v2.0+ -->
<template>
    <div class="bg-white">
        <div class="max-w-4xl mx-auto px-4 py-16 sm:px-6 sm:pt-20 sm:pb-24 lg:max-w-7xl lg:pt-24 lg:px-8">
            <div class="text-center mx-auto max-w-md px-4 sm:max-w-3xl sm:px-6 lg:px-8 lg:max-w-7xl">
                <p class="mt-2 text-3xl font-extrabold text-gray-900 tracking-tight sm:text-4xl">Metode Pembayaran</p>
                <p class="mt-5 mx-auto max-w-prose text-xl text-gray-500">Tersedia pilihan pembayaran yang dapat anda gunakan.</p>
            </div>
            <div class="mt-12 grid grid-cols-1 gap-x-6 gap-y-12 sm:grid-cols-2 lg:mt-16 lg:grid-cols-4 lg:gap-x-8 lg:gap-y-16">
                <div v-for="feature in features" :key="feature" class="flex justify-center items-center">
                    <img :src="feature.src" class="w-[70%] h-auto object-cover" />
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>

const features = [
    {
        src: 'https://privatalfaiz.id/images/2022/01/31/2-1-1024x576.png'
    },
    {
        src: 'https://privatalfaiz.id/images/2022/01/31/desain-tanpa-judul-1.png'
    },
    {
        src: 'https://1.bp.blogspot.com/-ENNeQXUXMPg/XwcgZZAcfRI/AAAAAAAAGlU/NdqxwMCYyNA49bSME2QHNmwJ-jBD-99PACK4BGAsYHg/s1000/logo-gopay.png'
    },
    {
        src: 'https://privatalfaiz.id/images/2022/01/31/permata.png',
    }
]

</script>