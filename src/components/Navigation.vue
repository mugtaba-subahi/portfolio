<template>
  <nav class="navigation-component">
    <ul class="nav">
      <li>
        <a @click="smoothScrollHandler" class="nav__item" href="#projects"> Projects </a>
      </li>
      <li>
        <a class="nav__item nav__item--resume" href="../CV.pdf" download> Resume </a>
      </li>
      <li>
        <a class="nav__item" target="_blank" href="https://github.com/DrSleepy"> GitHub </a>
      </li>
      <li>
        <a @click="smoothScrollHandler" class="nav__item" href="#contact"> Contact </a>
      </li>

    </ul>
  </nav>
</template>

<script>
export default {
  methods: {
    smoothScrollHandler() {
      event.preventDefault();
      const href = event.target.getAttribute('href');
      document.querySelector(href).scrollIntoView({ behavior: 'smooth', block: 'start' });
    }
  }
};
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
