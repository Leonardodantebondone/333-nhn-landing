<template>
  <UCard
    class="
      group
      bg-black/70
      border border-blue-400/50
      rounded-2xl
      p-4 sm:p-6
      flex flex-col
      items-center
      justify-center
      transition-all
      duration-500
      ease-out
      hover:-translate-y-2
      hover:scale-[1.02]
      hover:border-blue-400
      hover:shadow-xl
      hover:shadow-blue-500/50
    "
  >
    <!-- LOGO -->
    <div class="mb-3 sm:mb-4 flex items-center justify-center">
      <img
        v-if="icon"
        :src="icon"
        alt=""
        class="w-16 h-16 sm:w-20 sm:h-20 object-contain"
      />
    </div>

    <!-- TITOLO -->
    <h2
      class="text-blue-400 tracking-widest uppercase text-xs sm:text-sm mb-1 sm:mb-2 text-center"
    >
      {{ title }}
    </h2>

    <!-- TESTO -->
    <p
      class="text-white text-xs sm:text-sm opacity-90 text-center leading-relaxed mb-0 sm:mb-5"
    >
      {{ text }}
    </p>

    <!-- PULSANTE (SOLO DESKTOP) -->
    <a
      :href="link"
      target="_blank"
      class="
        hidden sm:inline-block
        mt-auto
        text-sm
        tracking-wide
        border border-blue-400
        px-5 py-2
        rounded-full
        transition-all
        duration-300
        ease-out
        hover:bg-blue-500
        hover:text-white
        hover:border-transparent
        hover:shadow-md
        hover:shadow-blue-500/50
        group-hover:bg-blue-500
        group-hover:text-white
      "
    >
      Apri
    </a>
  </UCard>
</template>

<script setup>
defineProps({
  title: String,
  text: String,
  link: String,
  icon: String
})
</script>
