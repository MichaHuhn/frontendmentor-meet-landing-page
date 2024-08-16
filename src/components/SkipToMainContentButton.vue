<script setup lang="ts">

</script>

<template>
  <a href="#main-content">Skip to main content</a>
</template>

<style scoped lang="scss">
a {
  --top: 1rem;
  --translateY: calc(-100% - var(--top));
  
  padding: var(--spacing-200) var(--spacing-500);
  color: black;
  background-color: white;
  border-radius: 100vmax;
  text-decoration: none;
  font-weight: bold;
  position: fixed;
  top: var(--top);
  left: 1rem;
  transform: translateY(var(--translateY));
  
  @media (prefers-reduced-motion: no-preference) {
    transition: transform 250ms ease;
  }
  
  &:focus {
    transform: translateY(0);
  }
}
</style>
