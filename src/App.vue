<script setup lang="ts">
import SkipToMainContentButton from '@/components/SkipToMainContentButton.vue';
import TheHeader from '@/components/TheHeader.vue';
import HeroSection from '@/components/hero-section/HeroSection.vue';
import TheMain from '@/components/TheMain.vue';
import TheFooter from '@/components/TheFooter.vue';
</script>

<template>
  <SkipToMainContentButton />
  
  <div class="home-view">
    <TheHeader />
    <HeroSection />
    <TheMain />
    <TheFooter />
  </div>
</template>

<style scoped lang="scss">
.home-view {
  --spacing-inline: var(--spacing-400);
}
</style>
