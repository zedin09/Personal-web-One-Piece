<template>
  <div class="about-me">
    <div class="about-me__content">
      <div class="about-me__content__left">
        <img
          class="about-me__content__left__img"
          src="../../assets/luffy2.jpg"
        />
      </div>
      <div class="about-me__content__right">
        <h3 class="about-me__content__right__title">Sobre mi</h3>
        <p class="about-me__content__right__text">
          Monkey D. Luffy es hijo de Monkey D. Dragon y nieto del almirante
          Garp, con apenas unos años comió una fruta del diablo y decidió que se
          convertiría en el rey de los piratas e iría en búsqueda del one piece.
        </p>
        <div>
          <vbutton-main
            texto="Linkedin"
            :text-color="color2"
            :background-color="color1"
          />
          <vbutton-main
            texto="GitHub"
            :text-color="color1"
            :background-color="color2"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VbuttonMain from "@/components/base/VbuttonMain";
import { colore1, colore2, coloreWhite } from "../_app.module.scss";

export default {
  name: "aboutMe",
  data() {
    return {
      color1: colore1,
      color2: colore2,
      colorWhite: coloreWhite,
    };
  },
  components: {
    VbuttonMain,
  },
};
</script>

<style lang="scss" scoped>
@import "../app.module";
.about-me {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 5em;
  padding-bottom: 5em;
  background: $color1;
  opacity: 0.95;
  &__content {
    width: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    &__left {
      border: 1px solid $color2;
      width: 150px;
      height: 200px;
      margin-right: 3em;
      &__img {
        width: 100%;
        height: 100%;
        position: relative;
        left: 20px;
        bottom: 20px;
      }
    }
    &__right {
      display: block;
      width: 40%;
      color: $color-white;
      &__title {
        font-family: $ff-primary;
        font-size: 20px;
        font-weight: bold;
        border-bottom: 2px solid $color2;
        margin-bottom: 1em;
        padding-bottom: 1em;
      }
      &__text {
        font-family: $ff-secondary;
        font-size: 15px;
        margin-bottom: 1.5em;
      }
    }
  }
}
</style>