<template>
  <section class="contact-display">
    <h2 class="sectionHeader">Get in touch</h2>
    <section class="contact-form-container">
      <div class="image-contact"></div>
      <contactForm></contactForm>
    </section>
  </section>
</template>

<script>
import contactForm from "./contact-form";
export default {
  components: {
    contactForm: contactForm
  }
};
</script>

<style lang="scss" scoped>
.contact-display {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  min-height: 100vh;
}
.contact-form-container {
  flex-grow: 1;
  display: flex;
  justify-content: center;
}

.image-contact {
  background: url("../assets/walking-in-vienna.png");
  flex-grow: 1;
  background-repeat: no-repeat;
  background-position: bottom;
  position: relative;
  width: 40%;

  &::before {
    content: "";
    height: 100%;
    width: 100%;
    background: rgb(191, 176, 163);
    background: linear-gradient(
      90deg,
      rgba(191, 176, 163, 0.1) 0%,
      rgba(93, 106, 115, 1) 100%
    );
    position: absolute;
    top: 0;
    left: 0;
    z-index: 2;
  }
}

@media screen and (max-width: 960px) {
  .image-contact {
    display: none;
  }
}
</style>