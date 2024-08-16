<script setup lang="ts">
import BaseButton from '@/components/BaseButton.vue';
</script>

<template>
  <div class="hero-text-content max-width-wrapper">
    <h1>
      Group Chat<br>
      for Everyone
    </h1>
    <p>Meet makes it easy to connect with others face-to-face virtually and collaborate across any device.</p>
    <div class="hero-actions">
      <BaseButton color="blue">
        <template #default>Download</template>
        <template #highlight>v1.3</template>
      </BaseButton>
      <BaseButton color="purple">What is it?</BaseButton>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import '@/assets/styles/base/typography';
@import '@/assets/styles/base/media-queries';

.hero-text-content {
  --max-width: var(--max-width-mobile);
  
  text-align: center;
  display: grid;
  gap: var(--spacing-300);
  
  @media #{$tablet-and-bigger} {
    width: 28rem;
  }
  
  @media #{$desktop-and-bigger} {
    gap: var(--spacing-400);
  }
  
  h1 {
    color: var(--color-slate-900);
    @include typography-mobile-1;
    
    @media #{$tablet-and-bigger} {
      @include typography-tablet-1;
    }
    
    @media #{$desktop-and-bigger} {
      @include typography-desktop-1;
    }
  }
  
  p {
    color: var(--color-slate-600);
    @include typography-tablet-4;
  }
  
  .hero-actions {
    display: flex;
    justify-content: center;
    gap: var(--spacing-200);
    flex-wrap: wrap;
  }
}
</style>
