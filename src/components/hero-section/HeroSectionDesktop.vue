<script setup lang="ts">
import HeroTextContent from '@/components/hero-section/HeroTextContent.vue';
</script>

<template>
  <section class="hero-section-desktop">
    <div class="wrapper">
      <img src="@/assets/images/desktop/hero-left.png" alt="">
      <HeroTextContent class="hero-text-content" />
      <img src="@/assets/images/desktop/hero-right.png" alt="">
    </div>
  </section>
</template>

<style scoped lang="scss">
@import '@/assets/styles/base/typography';
@import '@/assets/styles/base/media-queries';

.hero-section-desktop {
  padding-block: var(--spacing-800);
  
  .wrapper {
    height: 22.5rem;
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    align-items: center;
    gap: var(--spacing-400);
    overflow: hidden; /* Cut off images. They should leave the screen but that causes a horizontal scrollbar. */
    
    img {
      --offset: 6rem;
      --negative-offset: calc(var(--offset) * -1);
      
      height: calc(303 / 16 * 1rem);
      
      &:first-of-type {
        justify-self: end;
        align-self: start;
        transform: translateX(var(--negative-offset));
      }
      
      &:last-of-type {
        align-self: end;
        transform: translateX(var(--offset));
      }
    }
  }
}
</style>
