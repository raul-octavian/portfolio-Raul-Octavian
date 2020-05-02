.<template>
  <article id="hero-top">
    <h1>{{ textContent.name }}</h1>
    <h2>{{ textContent.activity }}</h2>
    <p id="top-one-text">
      {{ textContent.heroOne }}
      <br />
      {{ textContent.heroTwo}}
    </p>
    <p id="top-two-text">
      {{ textContent.heroThree }}
      <br />
      {{ textContent.heroFive }}
      <br />
      {{ textContent.heroSix }}
      <br />
      {{ textContent.heroSeven }}
    </p>
    <a href="#contact">
      <button>contact me</button>
    </a>
  </article>
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

#hero-top {
  z-index: 10;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  flex-direction: column;
}

h1 {
  padding-bottom: 10px;
  color: $Gravity---Sand-Creatures-II-1-rgba;
}

h2 {
  color: $Gravity---Sand-Creatures-II-5-rgba;
  padding-bottom: 100px;
  font-weight: 600;
}
#top-one-text,
#top-two-text {
  color: $Gravity---Sand-Creatures-II-5-rgba;
  padding-bottom: 30px;
  font-weight: 200;
}
#top-one-text {
  font-style: italic;
  font-weight: 400;
}

button {
  padding: 10px 30px;
  background-color: $Gravity---Sand-Creatures-II-1-rgba;
  border-radius: 30px;
  text-transform: uppercase;
  font-family: "Fira Sans", sans-serif;
  font-weight: 600;
}
a {
  text-decoration: none;
  font-weight: 600;
  color: $Gravity---Sand-Creatures-II-2-rgba;
}

@media screen and (max-width: 600px) {
  #hero-top {
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 100%;
  }
  #top-one-text,
  #top-two-text {
    text-align: center;
  }
}
</style>