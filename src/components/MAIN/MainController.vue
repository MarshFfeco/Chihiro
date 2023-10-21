<script setup lang="ts">
import ButtonCrontroller from '../BUTTON/ButtonController.vue';
</script>

<template>
  <div id="Main">
    <div
      id="Main--tittles"
      class="title"
    >
      <h2>HAYAO MIYAZAKI</h2>
      <h1>A VIAGEM<br> DE CHIHIRO</h1>
    </div>

    <div
      id="Main--content"
      class="content"
    >
      <p>Chihiro chega a um mundo mágico dominado por uma bruxa. Aqueles que a desobedecem são transformados em animais.</p>
    </div>

    <ButtonCrontroller class="button" />
  </div>
</template>

<style lang="scss" scoped>
  #Main {
    width: 445px;
    color: #F9F9F9;

    @media(max-width: 768px) {
      width: 100%
    }

    &--tittles {
      display: flex;
      flex-direction: column;
      gap: 14px;

      margin-bottom: 25px;

      h1 {
        font-size: 68px;
        font-weight: 900;
        line-height: 109%;

        @media(max-width: 768px) {
          font-size: 56px;
        }
      }

      h2 {
        font-size: 20px;
        font-weight: 700;

        @media(max-width: 768px) {
          font-size: 18px;
        }
      }
    }
  }
</style>
