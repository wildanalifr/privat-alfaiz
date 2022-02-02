<template>
  <NavbarHero />

  <div class="relative overflow-hidden">
    <main>
      <div class="relative bg-gray-100 py-10 section-info">
        <div class="mx-auto max-w-md px-4 text-center sm:max-w-3xl sm:px-6 lg:px-8 lg:max-w-7xl">
          <div class="grid grid-cols-1 gap-x-10 sm:grid-cols-2 lg:grid-cols-4">
            <div v-for="feature in features" :key="feature.name" class="pt-6">
              <div class="flex items-center justify-center flex-col p-10 bg-gray-300 rounded-md shadow-lg text-red-600 cursor-pointer hover:-translate-y-2 transition-transform">
                <component :is="feature.icon" class="h-16 w-h-16" aria-hidden="true" />
                <h3 class="mt-4 text-lg font-medium tracking-tight">{{ feature.name }}</h3>
              </div>
            </div>
          </div>
        </div>
      </div>

      <Why />

      <KelasPilihan />

      <TryOutTerbaru />

      <Testimonials />

      <Blog />

      <div class="bg-gray-50 py-16 sm:py-24 lg:py-32 relative">
        <div class="text-center mx-auto max-w-md px-4 sm:max-w-5xl sm:px-6 lg:px-8">
          <img src="https://privatalfaiz.id/images/2022/01/31/siap-1.jpg" class="rounded-md h-full" />
        </div>
      </div>

      <!-- Pembayaran Section -->
      <Pembayaran />
      <!-- Pembayaran Section -->

      <!-- FAQ Section -->
      <Faqs />
      <!-- FAQ Section -->

      <!-- CTA Section -->
      <Cta />
      <!-- CTA Section -->
    </main>

    <Footer />
  </div>
</template>

<script setup>
import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
import {
  AcademicCapIcon,
  CalendarIcon,
  CogIcon,
  LockClosedIcon,
  MenuIcon,
  RefreshIcon,
  ServerIcon,
  ShieldCheckIcon,
  XIcon,
} from '@heroicons/vue/outline'
import { ChevronRightIcon, ExternalLinkIcon } from '@heroicons/vue/solid'
import NavbarHero from './Parts/NavbarHero.vue'
import Faqs from './Parts/Faqs.vue'
import Blog from './Parts/Blog.vue'
import Footer from './Parts/Footer.vue'
import Why from './Parts/Why.vue'
import Cta from './Parts/Cta.vue'
import Pembayaran from './Parts/Pembayaran.vue'
import KelasPilihan from './Parts/KelasPilihan.vue'
import TryOutTerbaru from './Parts/TryOutTerbaru.vue'
import Testimonials from './Parts/Testimonials.vue'


const features = [
  {
    name: '5000+ Peserta',
    description: 'Ada lebih dari 5000 peserta baik calon CPNS atau calon Mahasiswa yang telah tergabung di Kursus Al Faiz',
    icon: AcademicCapIcon,
  },
  {
    name: 'Berdiri Sejak 2014',
    description: 'Sejak 2014, kami telah membantu ratusan mahasiswa dan calon cpns untuk meraih cita-cita yang di impikan',
    icon: CalendarIcon,
  },
  {
    name: 'Simple Queues',
    description: 'Rerum quas incidunt deleniti quaerat suscipit mollitia. Amet repellendus ut odit dolores qui.',
    icon: RefreshIcon,
  },
  {
    name: 'Advanced Security',
    description: 'Ullam laboriosam est voluptatem maxime ut mollitia commodi. Et dignissimos suscipit perspiciatis.',
    icon: ShieldCheckIcon,
  },

]

</script>

<style>
.section-info {
  background-image: url(../assets/background-red.jpg);
  background-attachment: fixed;
}
</style>