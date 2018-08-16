<template>
  <footer class="footer">
    <h2 class="title"> Contact </h2>
    <ul class="list">
      <li class="list__item list__item--email"> M-Subahi@hotmail.com </li>
      <li class="list__item list__item--linkedin"> Mugtaba Subahi </li>
      <li class="list__item list__item--github"> Dr Sleepy </li>
    </ul>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
@import (reference) './../styles/index.less';

.footer {
  .pad-8;
  background-color: @soft-grey-color;
  border-top: solid 1px @hard-grey-color;
  text-align: center;
}

.title {
  .push-down-5;
  .tera;
  color: @black-text-color;
  font-family: 'font-medium';
}

.list {
  &__item {
    .pad-2--5;

    &:before {
      .push-right-3;
      color: @soft-blue-color;
    }

    &--email:before {
      content: '@';
    }

    &--linkedin:before {
      content: '\f08c';
      font-family: FontAwesome;
    }

    &--github:before {
      content: '\f09b';
      font-family: FontAwesome;
    }
  }
}

// -------------------- media queries --------------------

@media @laptop {
  .footer {
    display: grid;
    grid-template-columns: auto auto;
    align-items: center;
  }

  .title {
    .push-down-0;
  }

  .list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }
}
</style>
