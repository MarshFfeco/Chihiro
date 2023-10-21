<script setup lang="ts">
import NavController from './components/NAV/NavController.vue';
import MainController from './components/MAIN/MainController.vue';
import ImageController from './components/IMAGE/ImageController.vue';
</script>

<template>
  <NavController />

  <section>
    <MainController class="main" />
    <ImageController class="image" />
  </section>
</template>

<style lang="scss" scoped>
  .main {
    margin-top: 75.89px;
  }

  section {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: 1fr;
    gap: 165px;

    @media(max-width: 1200px) {
      gap: 0;
    }

    @media(max-width: 768px) {
      grid-template-columns: 1fr;
      grid-template-rows: auto 1fr;
    }
  }

  .main {
    @media(max-width: 768px) {
      grid-row-start: 2;
      grid-row-end: 3;
    }
  }
  .image {
    @media(max-width: 768px) {
      grid-row-start: 1;
      grid-row-end: 2;
    }
  }
</style>
