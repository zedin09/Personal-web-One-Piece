<template>
  <div>
    <personal-data />
    <about-me />
    <personal-skills />
  </div>
</template>

<script>
import aboutMe from "@/components/home/aboutMe";
import personalData from "@/components/home/personalData";
import personalSkills from "@/components/home/personalSkills";

export default {
  name: 'App',
  components: {
    aboutMe,
    personalData,
    personalSkills,
  }
}
</script>

<style lang="scss">
* {
  margin: 0px;
  padding: 0px;
}
</style>
