<template>
  <section class="hero-container"></section>
</template>

<script>
export default {
  components: {}
};
</script>

<style lang="scss" scoped>
.hero-container {
  width: 40%;
  height: 100%;
  position: relative;
  background: url("../assets/hero-profile.png");
  background-repeat: no-repeat;
  background-position: bottom right;
  background-size: 100%;
  flex-grow: 1;
  position: absolute;
  right: 0;

  &:before {
    content: "";
    position: absolute;
    height: 100%;
    width: 100%;
    bottom: 0;
    left: 0;
    background: linear-gradient(
      140deg,
      rgba(17, 28, 38, 0.1) 0%,
      rgba(17, 28, 38, 1) 70%,
      rgba(17, 28, 38, 1) 100%
    );
    z-index: 6;
  }
}

@media screen and (max-width: 1000px) {
  .hero-container {
    display: none;
  }
}
</style>