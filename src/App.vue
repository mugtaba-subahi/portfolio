<template>
  <div class="root">
    <Navigation />

    <img class="wave wave--3" src="./assets/wave3.svg" alt="wave">
    <img class="wave wave--2" src="./assets/wave2.svg" alt="wave">
    <img class="wave wave--1" src="./assets/wave1.svg" alt="wave">

    <Introduction />
    <Skills />
    <Projects />

    <footer class="footer">
      <h2 class="title"> Contact </h2>
      <ul class="list">
        <li class="list__item list__item--email"> M-Subahi@hotmail.com </li>
        <li class="list__item list__item--linkedin"> Mugtaba Subahi </li>
        <li class="list__item list__item--github"> Dr Sleepy </li>
      </ul>
    </footer>

  </div>
</template>

<script>
import Navigation from './components/Navigation.vue';
import Introduction from './components/Introduction.vue';
import Skills from './components/Skills.vue';
import Projects from './components/Projects.vue';

export default {
  components: { Navigation, Introduction, Skills, Projects }
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
    .pad-2;

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

.root {
  position: relative;
  overflow-x: hidden;
  height: 100%;
}

.wave {
  position: absolute;
  z-index: -1;
  width: 180%;
  right: -50px;

  &--2 {
    margin-top: 25px;
  }

  &--1 {
    margin-top: 50px;
  }
}
</style>
