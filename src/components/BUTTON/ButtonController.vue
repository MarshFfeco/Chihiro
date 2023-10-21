<script setup lang="ts">
import {ref} from 'vue';

const isMinLength = ref(true);

window.addEventListener('resize', WinLength);

function WinLength() {
	if (window.innerWidth < 600) {
		isMinLength.value = false;
	} else {
		isMinLength.value = true;
	}
}
</script>

<template>
  <div id="Buttons">
    <button>
      <img
        src="../../assets/play.svg"
        alt=""
      > <p>ASSISTIR AGORA</p>
    </button>
    <Transition name="bounce">
      <button v-if="isMinLength">
        <p>ASSISTIR O TRAILER</p>
      </button>
    </Transition>
  </div>
</template>

<style lang="scss">
  #Buttons {
    width: 445px;
    margin-top: 46px;

    @media(max-width: 768px) {
      width: 100%
    }

    display: flex;
    justify-content: space-between;

    button {
      padding-inline: 32.25px;
      padding-block: 8px;

      transform: skewX(-15deg);

      &:first-child {
        display: flex;
        gap: 10px;
        align-items: center;

        padding-inline-start: 0px;
        padding-inline-end: 33px;

        border: 2px solid transparent;
        background-color: #658E76;

        img {
          margin-left: 17px;
        }
      }

      &:last-child {
        border: 2px solid #658E76;
      }

      :is(p, img) {
        transform: skewX(15deg);

        font-size: 16px;
        font-weight: 500;
        line-height: 180%
      }
    }
  }

  .bounce-enter-active {
    animation: bounce-in 0.5s;
  }
  .bounce-leave-active {
    animation: bounce-in 0.5s reverse;
  }
  @keyframes bounce-in {
    0% {
      transform: scale(0);
    }
    50% {
      transform: scale(1.25);
    }
    100% {
      transform: scale(1);
    }
  }
</style>
