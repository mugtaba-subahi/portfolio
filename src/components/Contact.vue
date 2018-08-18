<template>
  <footer class="footer">
    <h2 class="title"> Contact </h2>
    <ul class="list">
      <li class="list__item list__item--email">
        <a class="link" href="mailto:webmaster@example.com"> M-Subahi@hotmail.com </a>
      </li>
      <li class="list__item list__item--linkedin">
        <a class="link" target=" _blank " href="https://www.linkedin.com/in/msubahi-8328a4169/ "> Mugtaba Subahi </a>
      </li>
      <li class="list__item list__item--github ">
        <a class="link" target="_blank" href="https://github.com/DrSleepy"> Dr Sleepy </a>
      </li>
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

.link {
  color: @black-text-color;
}

// -------------------- media queries --------------------

@media @laptop {
  .footer {
    display: grid;
    grid-template-columns: auto auto;
    align-items: center;
    width: 1000px;
    justify-self: center;
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
