<template>
  <div class="personal-skills">
    <h3 class="personal-skills__title">Mis habilidades</h3>
    <p class="personal-skills__text">
      Estas son las principales habilidades que posee el futuro rey de los
      piratas
    </p>
    <div class="personal-skills__items">
      <div class="personal-skills__item" v-for="skill in skills" :key="skill.id">
        <vcard-main :title="skill.title" :content="skill.description" :color="skill.color"/>
      </div>
    </div>
  </div>
</template>

<script>
import { colore2, colore3, colore4, colore5 } from "../_app.module.scss";
import VcardMain from "@/components/base/VcardMain";

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "personalSkills",
  data() {
    return {
      skills: [
        {
          id: 0,
          title: "Kenbunshoku haki",
          description: "Agudiza el sentido de observación del usuario",
          color: colore2,
        },
        {
          id: 1,
          title: "Busoshoku haki",
          description:
            "Convierte el cuerpo en una armadura que si es lo suficientemente puede ser utilizada para atacar",
          color: colore3,
        },
        {
          id: 2,
          title: "Haoshoku haki",
          description:
            "Impone a fuerza de voluntad del usuario sobre todos alrededor, solo unos pocos lo poseen y quienes lo hacen están destinados a ser conquistadores",
          color: colore4,
        },
        {
          id: 3,
          title: "Gomu Gomu no mi",
          description:
            "Fruta del diablo que convierte el cuerpo del usuario en goma, recientemente se descubrió que es del tipo zoan modelo Nikka",
          color: colore5,
        },
      ],
      color2: colore2,
      color3: colore3,
      color4: colore4,
      color5: colore5,
    };
  },
  components: {
    VcardMain,
  },
};
</script>

<style lang="scss" scoped>
@import "../app.module";
.personal-skills {
  background: $color1;
  padding: 4em;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  &__title {
    font-family: $ff-primary;
    color: $color-white;
    margin-bottom: 1em;
    font-size: 24px;
  }
  &__text {
    font-family: $ff-secondary;
    color: $color-white;
    margin-bottom: 1em;
  }
  &__items {
    display: grid;
    grid-template-columns: 400px 400px;
  }
}
</style>
