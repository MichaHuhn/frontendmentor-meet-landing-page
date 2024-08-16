<script setup lang="ts">
const props = defineProps<{
  color: 'blue' | 'purple'
}>();
</script>

<template>
  <button :class="[props.color]">
    <span>
      <slot />
    </span>
    <span class="highlight" v-if="$slots.highlight">
      <slot name="highlight" />
    </span>
  </button>
</template>

<style scoped lang="scss">
@import '@/assets/styles/base/typography';

button {
  --background-color: var(--color-cyan-600);
  --background-color-hover: hsl(192deg 54% 64%);
  --highlight-color: var(--color-cyan-300);
  
  padding: var(--spacing-200) var(--spacing-500);
  color: var(--color-white);
  background-color: var(--background-color);
  @include typography-desktop-5;
  border: none;
  border-radius: 100vmax;
  cursor: pointer;
  
  &.blue {
    --background-color: var(--color-cyan-600);
    --background-color-hover: hsl(192deg 54% 64%);
    --highlight-color: var(--color-cyan-300);
  }
  
  &.purple {
    --background-color: var(--color-purple-600);
    --background-color-hover: hsl(268deg 55% 71%);
    --highlight-color: var(--color-purple-300);
  }
  
  &:hover, &:focus-visible {
    --background-color: var(--background-color-hover);
  }
  
  .highlight {
    color: var(--highlight-color);
    margin-inline-start: 0.375em;
  }
}
</style>
