<template>
  <nav>
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

.nav {
  .pad-4;
  margin-top: 10px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  justify-items: center;

  &__item {
    .milli;
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
