<template>
  <div class="relative overflow-hidden">

    <!-- SFONDO DINAMICO DARK -->
    <div class="fixed inset-0 -z-20">
      <div class="animated-dark-bg w-full h-full"></div>
    </div>

    <!-- SFONDO HERO IMAGE -->
    <div class="fixed inset-0 -z-10 overflow-hidden">
      <img src="/hero.jpeg" alt="Hero background" class="w-full h-full object-cover object-center" />
      <div class="absolute inset-0 bg-black/60"></div>
    </div>

    <!-- HERO: solo logo centrato -->
    <section class="relative z-10 h-[60vh] flex items-center justify-center text-center px-6 text-white">
      <AppLogo />
    </section>

    <!-- SEZIONE PULSANTE + CARDS -->
    <section class="relative z-10 max-w-6xl mx-auto px-6 py-16 sm:py-20 flex flex-col items-center">
      
      <!-- PULSANTE CENTRATO SOPRA LE CARDS -->
      <a href="mailto:nhn.333system@gmail.com"
         class="mb-12 inline-block px-8 py-4 bg-blue-700 text-white font-semibold rounded-full text-lg md:text-xl transition-all duration-400 hover:bg-blue-800 hover:scale-105 shadow-lg shadow-blue-900/50">
        Book a Gig / Contact
      </a>

      <!-- SOCIAL CARDS -->
      <div class="grid gap-8 sm:grid-cols-2 lg:grid-cols-3 w-full">
        <SocialCard title="Spotify" text="Release ufficiali e playlist curate." link="#" icon="/icons/spotify.svg" />
        <SocialCard title="SoundCloud" text="Set underground, demo e tracce non pubblicate." link="https://soundcloud.com/333-nhn" icon="/icons/soundcloud.svg" />
        <SocialCard title="Instagram" text="Identità visiva, eventi e lifestyle notturno." link="https://www.instagram.com/333_nhn/" icon="/icons/instagram.svg" />
        <SocialCard title="TikTok" text="Clip raw, momenti live e visioni oscure." link="https://www.tiktok.com/@333_nhn" icon="/icons/tiktok.svg" />
        <SocialCard title="Bandcamp" text="Supporta direttamente la musica." link="#" icon="/icons/bandcamp.svg" />
        <SocialCard title="YouTube" text="Set completi e visual experiment." link="#" icon="/icons/youtube.svg" />
      </div>
    </section>

    <!-- SOUND CLOUD PLAYER -->
    <section class="relative z-10 max-w-6xl mx-auto px-6 pb-16">
      <div class="w-full max-w-6xl mx-auto rounded-xl overflow-hidden shadow-lg bg-black/70 backdrop-blur">
        <iframe 
          width="100%" 
          height="200" 
          scrolling="no" 
          frameborder="no" 
          allow="autoplay" 
          src="https://w.soundcloud.com/player/?url=https%3A//soundcloud.com/333-nhn/333nhn-9mm&color=%23007bff&auto_play=true&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true">
        </iframe>
      </div>
    </section>

  </div>
</template>

<script setup>
import AppLogo from '~/components/AppLogo.vue'
import SocialCard from '~/components/SocialCard.vue'
</script>

<style scoped>
/* SFONDO DINAMICO DARK */
.animated-dark-bg {
  background: linear-gradient(270deg, #0b0b0f, #1a1a2e, #0d0d1a, #1a1a2e, #0b0b0f);
  background-size: 1000% 1000%;
  animation: darkGradientMove 40s ease-in-out infinite;
}

@keyframes darkGradientMove {
  0% { background-position: 0% 50%; }
  25% { background-position: 50% 50%; }
  50% { background-position: 100% 50%; }
  75% { background-position: 50% 50%; }
  100% { background-position: 0% 50%; }
}
</style>
