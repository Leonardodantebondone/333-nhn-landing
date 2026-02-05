<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>

<script setup>
useHead({
  htmlAttrs: { lang: 'en' },
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' },
    { name: 'theme-color', content: '#000000' }
  ],
  link: [
    { rel: 'icon', type: 'image/svg+xml', href: '/favicon.svg' },
    { rel: 'alternate icon', href: '/favicon.ico' }
  ]
})

useSeoMeta({
  title: '333 NHN',
  description: 'Official landing page of 333 NHN — dark, underground electronic music project.',
  ogTitle: '333 NHN',
  ogDescription: 'Dark & underground electronic music. Official links, releases and contact.',
  ogImage: '/og-image.jpg',
  ogType: 'website',
  twitterCard: 'summary_large_image',
  twitterTitle: '333 NHN',
  twitterDescription: 'Dark & underground electronic music project.',
  twitterImage: '/og-image.jpg'
})
</script>
