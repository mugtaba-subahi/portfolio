<template>
  <nav class="navigation-component">
    <ul class="nav">
      <li class="nav__item"> Projects </li>
      <li class="nav__item nav__item--resume"> Resume </li>
      <li class="nav__item"> GitHub </li>
      <li class="nav__item"> Contact </li>
    </ul>
  </nav>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
@import (reference) './../styles/index.less';
.navigation-component {
  display: grid;
  justify-content: center;
}

.nav {
  .pad-3--5;
  margin-top: 10px;
  display: grid;
  max-width: 600px;
  grid-template-columns: repeat(4, 1fr);
  justify-items: center;

  &__item {
    .milli;
    .pad-lr-1;
    color: #fff;
    font-family: 'font-medium';
    letter-spacing: 0.5px;

    &--resume:after {
      content: '\f019';
      font-family: FontAwesome;
      font-size: 13px;
      margin-left: 5px;
    }
  }
}

// -------------------- media queries --------------------

@media @tablet {
  .nav {
    &__item {
      .pad-lr-5;
    }
  }
}
</style>
