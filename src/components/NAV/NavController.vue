<template>
  <header>
    <nav id="navigation">
      <ul id="navigation--logo">
        <li>
          <img
            src="../../assets/logo.svg"
            alt="logo"
          >
        </li>
      </ul>
      <ul id="navigation--social">
        <li>
          <img
            src="../../assets/facebook.svg"
            alt="facebook"
          >
        </li>
        <li>
          <img
            src="../../assets/instagram.svg"
            alt="instagram"
          >
        </li>
        <li>
          <img
            src="../../assets/twitter.svg"
            alt="twitter"
          >
        </li>
        <li>
          <img
            src="../../assets/youtube.svg"
            alt="youtube"
          >
        </li>
      </ul>
    </nav>
  </header>
</template>

<style lang="scss">
  #navigation {
    display: flex;
    justify-content: space-between;

    &--social {
      display: flex;
      align-items: center;

      li {
        margin-right: 29px;

        &:last-child {
          margin-right: 0px;
        }
      }
    }

    li {
      cursor: pointer;
    }
  }
</style>
