<template>
  <section class="skills-component">
    <header class="header">
      <h2 class="header__title"> Skills </h2>
      <hr class="header__underline">
    </header>

    <div class="container">

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

    </div>

  </section>
</template>

<script>
export default {
  data() {
    return {
      languages: ['HTML', 'CSS', 'JavaScript', 'PHP', 'SQL', 'Java'],
      databases: ['MySQL', 'MongoDB', 'Firebase'],
      tools: ['Git/GitHub', 'VueJS', 'NodeJS', 'TypeScript', 'Stripe', 'GraphQL', 'APIs', 'REST API', 'PWA', 'Adobe XD']
    };
  }
};
</script>

<style lang="less" scoped>
@import (reference) './../styles/index.less';
.skills-component {
  .pad-lr-5;
}

.header {
  .header;
}

.wrapper {
  .push-down-10;

  &:last-child {
    .push-down-0;
  }
}

.subheading {
  .mega;
  .push-down-3;
  font-family: 'font-medium';
  color: @black-text-color;
}

.list {
  .list;

  &__item {
    color: @light-grey-text-color;

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

// -------------------- media queries --------------------

@media @tablet {
  .list {
    grid-template-columns: repeat(6, auto);
  }
}

@media @laptop {
  .list {
    grid-template-columns: repeat(7, auto);
  }

  .skills-component {
    display: grid;
  }
  .container {
    width: 800px;
    justify-self: center;
  }
}

@media @desktop {
  .list {
    grid-template-columns: repeat(9, auto);
  }
}
</style>
