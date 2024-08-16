<script setup lang="ts">
import HeroTextContent from '@/components/hero-section/HeroTextContent.vue';
</script>

<template>
  <section class="hero-section-mobile">
    <div class="hero-image">
      <img src="@/assets/images/desktop/hero-left.png" alt="">
      <img src="@/assets/images/desktop/hero-right.png" alt="">
    </div>
    
    <HeroTextContent class="hero-text-content" />
  </section>
</template>

<style scoped lang="scss">
@import '@/assets/styles/base/typography';
@import '@/assets/styles/base/media-queries';

.hero-section-mobile {
  padding-block: var(--spacing-800) var(--spacing-400);
  
  @media #{$tablet-and-bigger} {
    padding-block: var(--spacing-800);
  }
  
  .hero-image {
    height: 10rem;
    display: flex;
    justify-content: center;
    gap: calc(17 / 16 * 1rem);
    overflow: hidden; /* Cut off images. They should leave the screen but that causes a horizontal scrollbar. */
    
    @media #{$tablet-and-bigger} {
      height: calc(303 / 16 * 1rem);
      gap: 2rem;
    }
  }
  
  .hero-text-content {
    margin-block-start: var(--spacing-600);
    
    @media #{$tablet-and-bigger} {
      margin-block-start: var(--spacing-900);
    }
  }
}
</style>
