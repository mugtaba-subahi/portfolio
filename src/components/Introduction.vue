<template>
  <div>
    <h1 class="name"> Hi, I'm Mugtaba Subahi </h1>

    <div class="card">
      <h2 class="card__title"> Fullstack Web Developer </h2>
      <p class="card__text"> I have studied Computer Science at Kingston University and now building up my development skills to a professional level through personal projects </p>
      <img class="card__img" src="./../assets/plants.svg" alt="plants and books">
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="less" scoped>
@import (reference) './../styles/index.less';

.name {
  .exa;
  font-family: 'font-medium';
  color: white;
  margin-top: 130px;
  text-align: center;
}

.card {
  .box-shadow-1;
  margin: 8px;
  padding: @size-6 @size-6 @size-8 @size-6;
  background-color: white;
  position: relative;
  border-radius: 5px;
  text-align: center;

  &__title {
    .push-down-4;
    color: @light-blue-text-color;
  }

  &__text {
    color: @light-grey-text-color;
    letter-spacing: 0.2px;
  }

  &__img {
    position: absolute;
    bottom: -15px;
    right: 15px;
    width: 150px;
  }
}
</style>
