<template>
  <div class="root">
    <Navigation />

    <img class="waves" src="./assets/bluewaves.svg" alt="waves" />

    <h1 class="name">Hi, I'm Mugtaba Subahi</h1>
    <div class="card">
      <h2 class="card__title">Software Engineer</h2>

      <p class="card__text">
        Studied Computer Science at Kingston University whereafter I joined <strong>Association of Accounting Technicians (AAT)</strong> <br/> as a backend developer. <br/><br/> Completed two AWS certifications (Developer & Architect) before my journey led me to joining <strong>Dunelm</strong>, where I currently also work <br/> as a backend developer. 
      </p>

      <img class="card__img" src="./assets/plants.svg" alt="A set of plants and books" />
    </div>

    <Skills />
    <Projects id="projects" />
    <Contact id="contact" />
  </div>
</template>

<script>
import Navigation from "./components/Navigation.vue";
import Skills from "./components/Skills.vue";
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";

export default {
  components: { Navigation, Skills, Projects, Contact }
};
</script>

<style lang="less">
// Global styles
@import "./styles/reset.less";
@import "./styles/base.less";
</style>

<style lang="less" scoped>
// Scoped styles
@import (reference) "./styles/index.less";

.root {
  display: grid;
  position: relative;
  overflow-x: hidden;
  height: 100%;
}

.waves {
  position: absolute;
  z-index: -1;
  top: 0;
  right: 0;
  width: 200vw;
}

.name {
  .peta;
  margin: 30px 0;
  font-family: "font-medium";
  color: white;
  text-align: center;
  text-shadow: 0 1px 1px rgba(0, 0, 0, 0.15);
}

.card {
  .pad-tb-10;
  .pad-lr-5;
  .box-shadow-1;
  position: relative;
  justify-self: center;
  max-width: 780px;
  background-color: #fff;
  margin: @size-2--5;
  border-radius: 5px;
  text-align: center;

  &__title {
    .push-down-6;
    .giga;
    color: @light-blue-text-color;
  }

  &__text {
    color: @light-grey-text-color;
    font-family: "Roboto";
    max-width: 500px;
  }

  &__img {
    position: absolute;
    bottom: -15px;
    right: 15px;
    width: 150px;
  }
}

// -------------------- media queries --------------------

@media @tablet {
  .card {
    .pad-lr-10;
  }

  .waves {
    width: 125vw;
    top: -5vh;
  }
}

@media @laptop {
  .card {
    .pad-lr-10;
  }

  .waves {
    width: 100vw;
  }
}

@media @desktop {
  .waves {
    top: -5vh;
  }
}

@media @desktop-large {
  .waves {
    top: -20vh;
  }
}
</style>
