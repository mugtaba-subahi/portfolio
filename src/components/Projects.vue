<template>
  <section class="project-component">
    <header class="header">
      <h2 class="header__title">Projects</h2>
      <hr class="header__underline" />
    </header>

    <div class="gradients" v-for="(project, i) in projects" :key="i">
      <div class="project">
        <a :href="project.href" target="_blank">
          <img class="project__img" :src="project.img" :alt="project.alt" />
        </a>

        <div class="project__info">
          <h3 class="project__title">
            <a :href="project.href" target="_blank">{{ project.title }}</a>
          </h3>
          <p class="project__description" v-html="project.description">{{ project.description }}</p>
          <ul class="list">
            <li class="list__item" v-for="(tech, i) in project.list" :key="i">{{ tech }}</li>
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
          img: require("./../assets/flyguys.svg"),
          atl: "A preview of the Fly Guys website",
          title: "Fly Guys",
          href: "",
          description:
            "FlyGuys is a website that displays prices and details of flights. It consists of an admin dashboard to provide staff with CRUD operations (create, read, update and delete) on both flights and promotions. <br/> <br/> This was a university project that was undertaken in order to understand how payments are handled (using Stripe), how pure JS works on the frontend without a framework, the flow of PHP in an MVC structure as well as designing and using a relational database.",
          list: ["HTML", "CSS", "JavaScript", "PHP", "SQL", "MySQL", "Stripe"]
        },
        {
          img: require("./../assets/uth.svg"),
          atl: "A preview of JavaScript, Under the hood",
          title: "JavaScript, Under the Hood",
          href: "https://uth.netlify.com",
          description:
            "As it stands, this website explains how the JavaScript engine runs behind the scenes. This is a good read for those feeling rusty at JavaScript or want to test themselves a little on the languages itself. <br/> <br/> This was created to better solidify my understanding of the language by converting my notes into a website to have a place to often return to. My future plan is to keep adding notes as I progress through the language as well as add additional sections for different tools such as VueJS.",
          list: ["HTML", "CSS", "JavaScript", "VueJs", "PWA"]
        },
        {
          img: require("./../assets/salah.svg"),
          atl: "A preview of the Salah mobile website",
          title: "Salah",
          href: "",
          description:
            "Salah is a website that use a external APIs to retrieve data on Islamic prayer times given the user’s location. This project was designed to be used on mobiles phones. <br/> <br/> The purpose of the project, however, was to ease myself into using NodeJS, TypeScript and how PWA works with service workers.",
          list: [
            "HTML",
            "CSS",
            "JavaScript",
            "VueJs",
            "NodeJs",
            "TypeScript",
            "Firebase",
            "APIs",
            "PWA"
          ]
        },
        {
          img: require("./../assets/castleclash.svg"),
          atl: "A preview of the Castle Clash Hub website",
          title: "Castle Clash Hub",
          href: "https://castleclash.netlify.com/",
          description:
            "My goal for this project was to allow players of the game, Castle Clash, to have a place to list their in-game heroes and find other players with the same loadout. <br/> <br/> This was a personal (unfinished) project I picked up in my early days before understanding JS or CSS. My main purpose for developing this project was to try my hand at VueJS alongside a NoSQL database, Firebase RTDB.",
          list: ["HTML", "CSS", "JavaScript", "VueJs", "Firebase"]
        }
      ]
    };
  }
};
</script>

<style lang="less" scoped>
@import (reference) "./../styles/index.less";

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
    background: linear-gradient(
      rgba(252, 96, 118, 0.9),
      rgba(228, 54, 113, 0.7)
    );

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
  .pad-tb-10;
  .pad-lr-6;
  color: white;
  width: 100%;
  max-width: 500px;
  justify-self: center;
  text-shadow: 0 0.4px 0.4px rgba(0, 0, 0, 0.15);
  font-family: "Roboto";

  &__img {
    .push-down-4;
    .box-shadow-2;
    border-radius: 3px;
    width: 100%;
    transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);

    &:hover {
      cursor: pointer;
      box-shadow: 0 19px 28px rgba(0, 0, 0, 0.1), 0 12px 12px rgba(0, 0, 0, 0.1);
    }
  }

  &__title {
    .tera;
    .push-down-2;
    font-family: "font-medium";
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

    &__description {
      .kilo;
    }
  }
}

@media @desktop {
  .project-component {
    display: grid;
    justify-items: center;
  }
  .gradients {
    .push-down-5;
    .box-shadow-2;
    max-width: 1200px;
    border-radius: 3px;
  }
}
</style>
