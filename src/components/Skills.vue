<template>
  <section class="skills-component">
    <header class="header">
      <h2 class="header__title"> Skills </h2>
      <hr class="header__underline">
    </header>

    <div class="wrapper">
      <h3 class="subheading"> Languages </h3>
      <ul class="list">
        <li class="list__item list__item--languages" v-for="(language, i) in languages" :key="i"> {{ language }} </li>
      </ul>
    </div>

    <div class="wrapper">
      <h3 class="subheading"> Databases </h3>
      <ul class="list">
        <li class="list__item list__item--databases" v-for="(database, i) in databases" :key="i"> {{ database }} </li>
      </ul>
    </div>

    <div class="wrapper">
      <h3 class="subheading"> Tools </h3>
      <ul class="list">
        <li class="list__item list__item--tools" v-for="(tool, i) in tools" :key="i"> {{ tool }} </li>
      </ul>
    </div>

  </section>
</template>

<script>
export default {
  data() {
    return {
      languages: ['HTML', 'CSS', 'JavaScript', 'PHP', 'SQL', 'Java'],
      databases: ['MySQL', 'MongoDB', 'Firebase'],
      tools: ['Git/GitHub', 'VueJS', 'NodeJS', 'TypeScript', 'Stripe', 'GraphQL', 'REST API', 'PWA', 'Adobe XD']
    };
  }
};
</script>

<style lang="less" scoped>
@import (reference) './../styles/index.less';
.skills-component {
  .pad-tb-7;
  .pad-lr-5;
  background-color: #fff;
  border-top: solid 1px @hard-grey-color;
}

.header {
  .push-down-6;

  &__title {
    .title;
  }

  &__underline {
    .underline;
  }
}

.wrapper {
  .push-down-6;
}

.subheading {
  .mega;
  .push-down-3;
  font-family: 'font-medium';
  color: @black-text-color;
}

.list {
  .row-gap-1;
  display: grid;
  grid-template-columns: repeat(3, auto);

  &__item {
    color: @light-grey-text-color;

    &:before {
      .push-right-2;
      content: '';
      display: inline-block;
      height: 10px;
      width: 10px;
      border-radius: 3px;
    }

    &--languages:before {
      background-color: @soft-blue-color;
    }

    &--databases:before {
      background-color: @soft-green-color;
    }

    &--tools:before {
      background-color: @soft-pink-color;
    }
  }
}
</style>
