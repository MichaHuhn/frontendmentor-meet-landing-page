<script setup lang="ts">
import SectionNumber from '@/components/SectionNumber.vue';
import BaseButton from '@/components/BaseButton.vue';
</script>

<template>
  <footer>
    <SectionNumber class="section-number">02</SectionNumber>
    <div class="footer-hero">
      <div class="hero-background">
        <div class="hero-content max-width-wrapper">
          <h2 class="title">Experience more together</h2>
          <p class="description">Stay connected with reliable HD meetings and unlimited one-on-one and group video sessions.</p>
          <BaseButton color="purple">
            <template #default>Download</template>
            <template #highlight>v1.3</template>
          </BaseButton>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
@import '@/assets/styles/base/typography';
@import '@/assets/styles/base/media-queries';

footer {
  .section-number {
    margin-inline: auto;
    margin-block-end: calc(var(--number-wrapper-size) / 2 * -1);
    position: relative;
  }
  
  .footer-hero {
    background-image: url('@/assets/images/mobile/footer.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    
    @media #{$tablet-and-bigger} {
      background-image: url('@/assets/images/tablet/footer.jpg');
    }
    
    @media #{$desktop-and-bigger} {
      background-image: url('@/assets/images/desktop/footer.jpg');
    }
    
    .hero-background {
      background-color: hsl(from var(--color-cyan-600) h s l / 0.9);
      
      .hero-content {
        --max-width: var(--max-width-tablet-1);
        
        padding-block: var(--spacing-800);
        text-align: center;
        color: var(--color-white);
        @include typography-tablet-4;
        display: grid;
        justify-items: center;
        gap: var(--spacing-300);
        
        @media #{$desktop-and-bigger} {
          --max-width: var(--max-width-desktop);
          
          padding-block: var(--spacing-1400);
          text-align: revert;
          grid-template-columns: 5fr 4fr 3fr;
          align-items: start;
          gap: var(--spacing-400);
        }
        
        .title {
          @include typography-mobile-2;
          
          @media #{$tablet-and-bigger} {
            @include typography-tablet-2;
          }
          
          @media #{$desktop-and-bigger} {
            @include typography-desktop-2;
          }
        }
        
        .description {
          @include typography-tablet-4;
          
          @media #{$desktop-and-bigger} {
            @include typography-desktop-4;
          }
        }
        
        @media #{$desktop-and-bigger} {
          & > :last-child {
            justify-self: end;
          }
        }
      }
    }
  }
}
</style>
