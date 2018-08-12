<template>
  <div id="app">
    <nav>
      <ul class="nav">
        <li class="nav__item"> Projects </li>
        <li class="nav__item nav__item--resume"> Resume </li>
        <li class="nav__item"> GitHub </li>
        <li class="nav__item"> Contact </li>
      </ul>
    </nav>

    <img class="wave" src="./assets/wave1.svg" alt="wave">
    <img class="wave" src="./assets/wave2.svg" alt="wave">
    <img class="wave" src="./assets/wave3.svg" alt="wave">

    <h1 class="name"> Hi, I'm Mugtaba Subahi </h1>
    <div class="card">
      <h2 class="card__title"> Fullstack Web Developer </h2>
      <p class="card__text"> I have studied Computer Science at Kingston University and now building up my development skills to a professional level through personal projects </p>
      <img class="card__img" src="./assets/plants.svg" alt="plants and books">
    </div>
  </div>
</template>

<script>
export default {
  components: {}
};
</script>

<style lang="less">
// Global styles
@import './styles/reset.less';
@import './styles/base.less';
</style>

<style lang="less" scoped>
// Scoped styles
@import (reference) './styles/index.less';

.nav {
  .pad-tb-7;
  .pad-lr-4;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  justify-items: center;

  &__item {
    color: @light-blue-text-color;
    font-family: 'font-medium';

    &--resume:after {
      content: '\f019';
      font-family: FontAwesome;
      font-size: 13px;
      margin-left: 5px;
    }
  }
}
</style>
