<template>
  <section id="paralax-image">
    <div>
      <img src="../assets/hero-profile.png" alt />
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#paralax-image {
  grid-area: image;
}

div {
  position: sticky;
  top: 100px;

  &::before {
    content: "";
    height: 102%;
    width: 102%;
    position: absolute;
    z-index: 1;
    background: rgb(239, 239, 239);
    background: linear-gradient(
      340deg,
      rgba(239, 239, 239, 1) 0%,
      rgba(239, 239, 239, 1) 35%,
      rgba(239, 239, 239, 0) 100%
    );
  }
}

img {
  width: 90%;
  position: sticky;
}

@media only screen and (max-width: 650px) {
  #paralax-image {
    display: none;
  }
}
</style>