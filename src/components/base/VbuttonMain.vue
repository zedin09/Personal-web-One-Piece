<template>
  <a
    class="main-btn"
    href="#"
    :style="{ background: backgroundColor, color: textColor }"
  >
    {{ texto }}
  </a>
</template>

<script>
export default {
  name: "VbuttonMain",
  props: {
    texto: String,
    textColor: String,
    backgroundColor: String,
  },
};
</script>

<style lang="scss" scoped>
@import "../app.module";
.main-btn {
  padding: 7px 20px 7px 20px;
  font-family: $ff-secondary;
  border: 1px solid;
  margin: 5px;
  text-decoration: none;
}
</style>
