<template>
  <nav class="navigation-component">
    <ul class="nav">
      <li>
        <a @click="smoothScrollHandler" class="nav__item" href="#projects">Projects</a>
      </li>
      <li>
        <a
          class="nav__item"
          target="_blank"
          href="https://drive.google.com/file/d/153v31Ubj58XOPFXrd_AOEChEI6B0LM0V/view?usp=sharing"
          download
        >Resume</a>
      </li>
      <li>
        <a class="nav__item" target="_blank" href="https://github.com/mugtaba-subahi">GitHub</a>
      </li>
      <li>
        <a @click="smoothScrollHandler" class="nav__item" href="#contact">Contact</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  methods: {
    smoothScrollHandler() {
      event.preventDefault();
      const href = event.target.getAttribute("href");
      document
        .querySelector(href)
        .scrollIntoView({ behavior: "smooth", block: "start" });
    }
  }
};
</script>

<style lang="less" scoped>
@import (reference) "./../styles/index.less";
.navigation-component {
  display: grid;
}

.nav {
  .pad-3--5;
  margin-top: 10px;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  justify-items: center;

  &__item {
    .milli;
    .pad-lr-1;
    font-family: "font-medium";
    letter-spacing: 0.5px;
  }
}

// -------------------- media queries --------------------

@media @tablet {
  .nav {
    justify-self: center;

    &__item {
      .pad-lr-5;
      .kilo;
    }
  }
}
</style>
