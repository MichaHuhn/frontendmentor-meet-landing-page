<script setup lang="ts">
import SectionNumber from '@/components/SectionNumber.vue';
</script>

<template>
  <main id="main-content">
    <div class="main-content max-width-wrapper">
      <SectionNumber>01</SectionNumber>
      
      <div class="image-collage">
        <img src="@/assets/images/desktop/woman-in-videocall.jpg" alt="A woman is in a videocall">
        <img src="@/assets/images/desktop/women-videochatting.jpg" alt="Women are video chatting">
        <img src="@/assets/images/desktop/men-in-meeting.jpg" alt="Men are in a videocall meeting">
        <img src="@/assets/images/desktop/man-texting.jpg" alt="A man is texting">
      </div>
      
      <article class="text-content">
        <p class="subtitle">Built for modern use</p>
        <h2 class="title">Smarter meetings, all in one place</h2>
        <p class="description">
          Send messages, share files, show your screen, and record your meetings — all in one
          workspace. Control who can join with invite-only team access, data encryption, and data export.
        </p>
      </article>
    </div>
  </main>
</template>

<style scoped lang="scss">
@import '@/assets/styles/base/typography';
@import '@/assets/styles/base/media-queries';

main {
  padding-block: var(--spacing-400) var(--spacing-800);
  
  @media #{$tablet-and-bigger} {
    padding-block: var(--spacing-700) var(--spacing-800);
  }
  
  @media #{$desktop-and-bigger} {
    padding-block: var(--spacing-700) var(--spacing-900);
  }
  
  .main-content {
    --max-width: var(--max-width-tablet-2);
    
    text-align: center;
    display: grid;
    justify-items: center;
    gap: var(--spacing-800);
    
    @media #{$desktop-and-bigger} {
      --max-width: var(--max-width-desktop);
    }
    
    .image-collage {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: var(--spacing-200);
      
      @media #{$tablet-and-bigger} {
        grid-template-columns: revert;
        grid-auto-flow: column;
        gap: var(--spacing-300);
      }
      
      @media #{$desktop-and-bigger} {
        gap: var(--spacing-400);
      }
      
      img {
        border-radius: 8px;
      }
    }
    
    .text-content {
      max-width: var(--max-width-tablet-1);
      display: grid;
      justify-items: center;
      
      @media #{$desktop-and-bigger} {
        max-width: 34rem;
      }
      
      .subtitle {
        color: var(--color-cyan-600);
        @include typography-mobile-3;
        text-transform: uppercase;
        
        @media #{$tablet-and-bigger} {
          @include typography-tablet-3;
        }
        
        @media #{$desktop-and-bigger} {
          @include typography-desktop-3;
        }
      }
      
      .title {
        max-width: calc(445 / 16 * 1rem);
        margin-block-start: var(--spacing-200);
        color: var(--color-slate-900);
        @include typography-mobile-2;
        
        @media #{$tablet-and-bigger} {
          @include typography-tablet-2;
        }
        
        @media #{$desktop-and-bigger} {
          @include typography-desktop-2;
        }
      }
      
      .description {
        margin-block-start: var(--spacing-400);
        color: var(--color-slate-600);
        @include typography-tablet-4;
        
        @media #{$desktop-and-bigger} {
          @include typography-desktop-4;
        }
      }
    }
  }
}
</style>
