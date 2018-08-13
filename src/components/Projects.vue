<template>
  <section class="project-component">
    <header class="header">
      <h2 class="header__title"> Projects </h2>
      <hr class="header__underline">
    </header>

    <div class="gradients" v-for="(project, i) in projects" :key="i">
      <div class="project">
        <img class="project__img" :src="project.img" :alt="project.alt">
        <div class="project__info">
          <h3 class="project__title"> {{ project.title }} </h3>
          <p class="project__description"> {{ project.description }} </p>
          <ul class="list">
            <li class="list__item" v-for="(tech, i) in project.list" :key="i"> {{ tech }} </li>
          </ul>
        </div>
      </div>
    </div>

  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          img: require('./../assets/flyguys.svg'),
          atl: 'A preview of the Fly Guys website',
          title: 'Fly Guys',
          description: 'A site for flights',
          list: ['HTML', 'CSS', 'JavaScript', 'PHP', 'SQL', 'MySQL', 'Stripe']
        },
        {
          img: require('./../assets/uth.svg'),
          atl: 'A preview of JavaScript, Under the hood',
          title: 'JavaScript, Under the Hood',
          description: 'For those needing a refresher at JavaScript',
          list: ['HTML', 'CSS', 'JavaScript', 'VueJs', 'PWA']
        },
        {
          img: require('./../assets/salah.svg'),
          atl: 'A preview of the Salah mobile website',
          title: 'Salah',
          description: 'A tracker and reminder for your islamic prayers',
          list: ['HTML', 'CSS', 'JavaScript', 'VueJs', 'NodeJs', 'TypeScript', 'Firebase', 'APIs', 'PWA']
        },
        {
          img: require('./../assets/castleclash.svg'),
          atl: 'A preview of the Castle Clash Hub website',
          title: 'Castle Clash Hub',
          description: 'An (unfinished) hub for all Castle Clash players',
          list: ['HTML', 'CSS', 'JavaScript', 'VueJs', 'Firebase']
        }
      ]
    };
  }
};
</script>

<style lang="less" scoped>
@import (reference) './../styles/index.less';

.header {
  .header;
  padding-top: 120px;
  padding-bottom: 60px;
  background: #fff;
}

.gradients {
  display: grid;

  // Fly Guys
  &:nth-of-type(1) {
    background: linear-gradient(rgba(143, 148, 251, 0.7), #ef93ec);

    .list__item:before {
      background-color: #95e8c3;
    }
  }

  // JavaScript,Under the Hood
  &:nth-of-type(2) {
    background: linear-gradient(#005bea, #00c6fb);

    .list__item:before {
      background-color: #fce631;
    }
  }

  // Salah
  &:nth-of-type(3) {
    background: linear-gradient(rgba(252, 96, 118, 0.9), rgba(228, 54, 113, 0.7));

    .list__item:before {
      background-color: #95e8c3;
    }
  }

  // Castle Clash Hub
  &:nth-of-type(4) {
    background: linear-gradient(#fbc8d4, rgba(213, 69, 165, 0.77));

    .list__item:before {
      background-color: #03aaf9;
    }
  }
}

.project {
  .pad-6;
  color: white;
  width: 100%;
  max-width: 500px;
  justify-self: center;

  &__img {
    .push-down-4;
    border-radius: 3px;
    width: 100%;
    box-shadow: 0 5px 20px rgba(86, 18, 142, 0.1), 0 3px 30px rgba(86, 18, 142, 0.2);
  }

  &__title {
    .push-down-2;
    font-family: 'font-medium';
  }

  &__description {
    .milli;
    .push-down-5;
  }
}

.list {
  .list;
}

// -------------------- media queries --------------------

@media @laptop {
  .project {
    .gap-8;
    margin: 70px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    max-width: 1000px;
  }
}
</style>
