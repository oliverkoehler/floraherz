<template>
  <div class="bg-[#001910]/75 h-[100vh] w-[100vw] grid">
    <div class="w-[100vw] flex flex-col items-center">
      <div class="font-semibold text-[#CED8CE] text-4xl text-center pt-10">
        Floraherz
      </div>
      <div class="font-semibold text-[#CED8CE] text-2xl text-center">
        Sandra Frangen
      </div>
      <div class="text-white/90 max-w-[550px] text-center mt-6 mx-8">
        Hallo ihr Lieben, danke das ihr auf meiner Seite vorbeischaut. Hier findet ihr alle wichtigen Links zu meinen Social Media Kanälen und meinem Etsy Webshop. Viel Spaß beim Stöbern! 🌸
      </div>
    </div>
    <div class="">
      <div class="w-full md:flex flex-col items-center">
        <AppLink v-for="(link, i) in links" :key="i" :to="link.to" :name="link.name" :color="link.color"
                 :image="link.image" />
      </div>
    </div>

    <div class="text-center text-gray-300 mx-3">
      <div>
        Sandra Frangen |
        Floraherz | 2024
      </div>
      <div>
        Marktstraße 23, 56330 Kobern-Gondorf
      </div>
      <div>
        <a class="underline cursor-pointer" href="mailto:frangen.sandra@gmail.com">frangen.sandra@gmail.com</a>
      </div>
      <div>
        Made with ❤️ by Oliver Köhler
      </div>
    </div>
  </div>
</template>

<script setup>

import AppLink from "@/components/AppLink.vue";

const links = [
  { to: 'https://www.etsy.com/shop/Floraherz?ref=floraherz.de', name: 'Etsy Webshop', color: 'bg-red-300', image: 'https://i.etsystatic.com/isla/12e5ab/71617295/isla_280x280.71617295_kjyo1y7b.jpg?version=0' },
  { to: 'https://www.ebay.de/usr/floraherz', name: 'Ebay Webshop', color: 'bg-yellow-300', image:
      'https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/EBay_logo.svg/2000px-EBay_logo.svg.png' },
  { to: 'https://itrk.legal/R4I.76.KRp.html', name: 'Instagram AGBs', color: 'bg-blue-300', image: 'https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/Instagram_logo_2016.svg/2048px-Instagram_logo_2016.svg.png' },
  { to: 'https://itrk.legal/R4I.8t.KRp.html', name: 'TikTok AGBs', color: 'bg-green-300', image: 'https://cdn.pixabay.com/photo/2021/06/15/12/28/tiktok-6338429_1280.png' },
]
</script>
