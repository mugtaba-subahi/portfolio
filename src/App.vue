<template>
  <div class="root">
    <Navigation />

    <img class="wave wave--3" src="./assets/wave3.svg" alt="wave">
    <img class="wave wave--2" src="./assets/wave2.svg" alt="wave">
    <img class="wave wave--1" src="./assets/wave1.svg" alt="wave">

    <Introduction />
    <Skills />
    <Projects />
    <Contact />
  </div>
</template>

<script>
import Navigation from './components/Navigation.vue';
import Introduction from './components/Introduction.vue';
import Skills from './components/Skills.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';

export default {
  components: { Navigation, Introduction, Skills, Projects, Contact }
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
