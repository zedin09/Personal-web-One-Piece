<template>
  <div class="card-main" :style="{ background: color }">
    <h4 class="card-main__title">{{ title }}</h4>
    <p class="card-main__text">{{ content }}</p>
  </div>
</template>

<script>
export default {
  name: "VcardMain",
  props: {
    title: String,
    content: String,
    color: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../app.module";
  .card-main {
    width: 300px;
    height: 120px;
    padding: 2em;
    color: $color-white;
    margin: 10px;
    &__title {
      font-family: $ff-primary;
      font-size: 20px;
      margin-bottom: 1em;
    }
    &__text {
      font-family: $ff-secondary;
    }
  }
</style>
