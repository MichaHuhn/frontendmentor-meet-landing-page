<script setup lang="ts">
import HeroSectionMobile from '@/components/hero-section/HeroSectionMobile.vue';
import HeroSectionDesktop from '@/components/hero-section/HeroSectionDesktop.vue';
</script>

<template>
  <HeroSectionMobile class="hero-section-mobile" />
  <HeroSectionDesktop class="hero-section-desktop" />
</template>

<style scoped lang="scss">
@import '@/assets/styles/base/media-queries';

.hero-section-desktop {
  display: none;
}

@media #{$desktop-and-bigger} {
  .hero-section-mobile {
    display: none;
  }
  
  .hero-section-desktop {
    display: revert;
  }
}
</style>
