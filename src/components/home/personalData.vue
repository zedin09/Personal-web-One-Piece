<template>
  <div class="personal-data">
    <div class="personal-data__left">
      <div class="personal-data__left__content">
        <span class="personal-data__left__content__text">Hola</span>
        <h3 class="personal-data__left__content__name">Yo soy Monkey D. Luffy</h3>
        <p class="personal-data__left__content__description">
          Soy el capitán de los piratas sombrero de paja, he comido la gomu gomu
          no mi y me convertiré en el futuro rey de los piratas cuando encuentre
          el one piece.
        </p>
        <vbutton-main
          texto="Contactar"
          :text-color="color2"
          :background-color="color1"
        />
      </div>
    </div>
    <div class="personal-data__right">
      <img class="personal-data__right__img" src="../../assets/luffy1.png" />
    </div>
  </div>
</template>

<script>
  import VbuttonMain from "@/components/base/VbuttonMain";
  import { colore1, colore2 } from "../_app.module.scss"

  export default {
    name: "personalData",
    data() {
      return {
        color1: colore1,
        color2: colore2,
      }
    },
    components: {
      VbuttonMain,
    },
  };
</script>

<style lang="scss" scoped>
@import "../app.module";
.personal-data {
  display: flex;
  width: 100%;
  &__left {
    background: $color1;
    width: 60%;
    display: flex;
    justify-content: center;
    align-items: center;
    &__content {
      width: 300px;
      color: $color-white;
      &__text {
        font-family: $ff-secondary;
        font-size: 14px;
        margin-bottom: 10px;
      }
      &__name {
        font-family: $ff-primary;
        font-size: 24px;
        color: $color2;
        margin-bottom: 10px;
      }
      &__description {
        font-family: $ff-secondary;
        font-size: 15px;
        margin-bottom: 2em;
      }
    }
  }
  &__right {
    background: $color2;
    width: 40%;
    &__img {
      width: 200px;
      position: relative;
      left: -100px;
    }
  }
}
</style>
