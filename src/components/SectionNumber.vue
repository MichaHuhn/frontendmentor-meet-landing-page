<script setup lang="ts">

</script>

<template>
  <div class="section-number" aria-hidden="true">
    <div class="line"></div>
    <div class="number-wrapper">
      <div class="number"><slot /></div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import '@/assets/styles/base/typography';

.section-number {
  --border-color: var(--color-slate-300);
  --number-wrapper-size: 3.5rem;
  
  width: fit-content;
  display: grid;
  justify-items: center;
  
  .line {
    width: 1px;
    height: 5rem;
    background-color: var(--border-color);
  }
  
  .number-wrapper {
    width: var(--number-wrapper-size);
    height: var(--number-wrapper-size);
    background-color: var(--color-white);
    border: 1px solid var(--border-color);
    border-radius: 100vmax;
    @include typography-desktop-5;
    display: grid;
    place-content: center;
    
    .number {
      color: var(--color-slate-600);
      transform: translateY(1px); /* optical alignment */
    }
  }
}
</style>
