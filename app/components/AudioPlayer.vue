<template>
  <div class="flex flex-col md:flex-row items-center gap-6 p-6 bg-gradient-to-r from-black/70 to-black/50 border border-blue/40 rounded-2xl shadow-xl w-full max-w-6xl">
    <!-- COPERTINA -->
    <div class="flex-shrink-0 w-48 md:w-56">
      <img :src="cover" alt="Cover" class="w-full h-full object-cover rounded-2xl shadow-2xl border border-blue/30" />
    </div>

    <!-- INFO + AUDIO -->
    <div class="flex-1 flex flex-col justify-center h-full w-full">
      <h3 class="text-white text-2xl md:text-3xl font-bold mb-4 text-center md:text-left">{{ title }}</h3>
      <audio ref="audioRef" :src="src" autoplay controls class="w-full"></audio>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'

defineProps({ title: String, src: String, cover: String })
const audioRef = ref(null)

onMounted(() => {
  if (audioRef.value) audioRef.value.play().catch(() => console.log('Autoplay bloccato dal browser'))
})
</script>
