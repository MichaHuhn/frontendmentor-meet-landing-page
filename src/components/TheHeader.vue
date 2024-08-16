<script setup lang="ts">

</script>

<template>
  <header>
    <nav>
      <ul>
        <li>
          <a href="#">
            <img src="@/assets/images/logo.svg" alt="meet logo">
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped lang="scss">
@import '@/assets/styles/base/media-queries';

header {
  padding-block-start: var(--spacing-600);
  display: flex;
  justify-content: center;
  
  @media #{$desktop-and-bigger} {
    padding-block-start: var(--spacing-1000);
  }
  
  ul {
    padding: 0;
    list-style: none;
  }
}
</style>
