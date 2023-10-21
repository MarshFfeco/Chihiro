<template>
  <div id="Image">
    <img
      src="../../assets/image.png"
      alt="imagem fantasma"
    >
  </div>
</template>

<style lang="scss">
  #Image {
    display: flex;
    justify-content: center;
    align-items: center;
    img {
      width: 100%;

      @media(max-width: 768px) {
        width: 221px;
      }
    }
    animation: voar 2s linear infinite;
  }

  @keyframes voar {
      0%, 100% {transform: translateY(0);}
      50% {transform: translateY(50px);}
  }
</style>
