<template>
  <section class="about-text-container">
    <h3>{{ textContent.aboutTitle }}</h3>
    <p class="about-text">{{ textContent.aboutOne }}</p>

    <p class="about-text">{{ textContent.aboutTwo }}</p>

    <p class="about-text">{{ textContent.aboutThree }}</p>
    <p class="about-text">{{ textContent.aboutFour }}</p>
  </section>
</template>

<script>
export default {
  props: {
    textContent: Object
  }
};
</script>

<style lang="scss" scoped>
@import url("../styles/variables.scss");
.about-text-container {
  background-color: $Gravity---Sand-Creatures-II-5-rgba;
  padding: 50px 50px;
  min-height: 65vh;
}

h3 {
  color: $Gravity---Sand-Creatures-II-1-rgba;
  font-size: $font-size-medium;
  margin-bottom: 50px;
}
.about-text {
  color: $Gravity---Sand-Creatures-II-2-rgba;
  margin-bottom: 20px;
  font-weight: 200;
}
</style>