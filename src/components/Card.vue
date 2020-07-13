<template>
  <article class="bigCard">
    <section class="shadow card">
      <div class="img-container">
        <div class="project-image">
          <img :src="image" />
        </div>
        <h4>{{ name }}</h4>
      </div>
      <p class="card-text">{{ dSmall }}</p>
      <a class="flex">
        <button @click="showCard = !showCard" class="read-more">
          Read more
        </button>
      </a>
    </section>
    <section
      v-show="showCard"
      class="description"
      @click="showCard = !showCard"
    >
      <h4>{{ name }}</h4>
      <p>{{ description }}</p>
      <p>{{ dTwo }}</p>
      <div class="contact bottom">
        <a :href="sourceLink" target="blank">
          <button>Source</button>
        </a>
        <a :href="activeLink" target="blank">
          <button>Active website</button>
        </a>
      </div>
    </section>
  </article>
</template>

<script>
export default {
  data() {
    return {
      showCard: false
    };
  },
  methods: {},
  props: {
    name: String,
    dSmall: String,
    description: String,
    dTwo: String,
    sourceLink: String,
    activeLink: String,
    image: String
  }
};
</script>

<style lang="scss" scoped>
article {
  max-width: 100%;
  display: flex;
}
.description {
  flex-grow: 1;
  padding: 20px 40px;
  margin: 20px 0;
  position: absolute;
  left: 15vw;
  background-color: rgba(
    $color: $Gravity---Sand-Creatures-II-3-hex,
    $alpha: 0.9
  );
  color: $Gravity---Sand-Creatures-II-5-rgba;
  height: 60vh;
  width: 70vw;
  z-index: 90;
  border: 3px solid white;
  margin: 20px;

  h4 {
    margin-bottom: 40px;
    color: $Gravity---Sand-Creatures-II-5-rgba;
  }
  p {
    margin-bottom: 20px;
    font-size: $font-size-normal-tablet;
    color: $Gravity---Sand-Creatures-II-5-rgba;
  }
}

.bottom {
  position: absolute;
  bottom: 40px;
  button {
    &:nth-child(1) {
      margin-right: 20px;
    }
  }
}

.card {
  height: 500px;
  min-width: 350px;
  width: 350px;
  background: $Gravity---Sand-Creatures-II-5-rgba;
  padding: 20px 40px;
  transition: all 500ms ease-in-out;
  border: 3px solid white;
  margin: 20px;
  position: relative;

  &:hover {
    transform: translateY(3px);
  }
}
a {
  text-decoration: none;
  color: $Gravity---Sand-Creatures-II-2-rgba;
  width: 100%;
}
.flex {
  display: flex;
  justify-content: center;
  align-items: center;
}

.img-container {
  width: 100%;
  height: 55%;
  display: flex;
  flex-direction: row;
  justify-content: center;
  flex-wrap: wrap;
  padding: 10px 0;
  img {
    width: 100%;
    height: 100%;
  }
}
.project-image {
  background-position: center;
  background-size: cover;
  width: 100%;
  height: 90%;
  border: 2px solid white;
}
h4 {
  font-weight: 500;
  align-self: flex-end;
  padding-top: 10px;
  color: $Gravity---Sand-Creatures-II-2-rgba;
}

.shadow {
  transition: all 500ms ease-in-out;
  &:hover {
    box-shadow: 0.3rem 0.3rem 1rem rgba(0, 0, 0, 0.3),
      -0.3rem -0.3rem 1rem rgba(255, 255, 255, 0.5),
      inset 0.2rem 0.2rem 0.5rem rgba(0, 0, 0, 0.2),
      inset -0.2rem -0.2rem 0.5rem rgba(255, 255, 255, 1);
  }
}

.card-text {
  padding: 30px 0;
  text-align: center;
  font-weight: 300;
  z-index: 5;
}
button {
  padding: 10px 30px;
  background-color: $Gravity---Sand-Creatures-II-1-rgba;
  border-radius: 30px;
  text-transform: uppercase;
  font-family: "Fira Sans", sans-serif;
  font-weight: 600;
}
.read-more {
  z-index: 5;
  position: absolute;
  bottom: 40px;
}

@media screen and (max-width: 1100px) {
  article {
    flex-direction: column;
    justify-content: center;
  }
  .description {
    flex-grow: 1;
    padding: 20px 0;
    margin: 20px 0;
    position: relative;
    h4 {
      margin-bottom: 40px;
    }
    p {
      margin-bottom: 20px;
      font-size: $font-size-normal-tablet;
    }
  }
  .bottom {
    position: initial;
    bottom: initial;
    button {
      &:nth-child(1) {
        margin: 20px 20px 20px 0;
      }
    }
  }
  .card {
    height: 420px;
    min-width: 320px;
    width: 320px;
    background: $Gravity---Sand-Creatures-II-5-rgba;
    padding: 20px 40px;
    transition: all 500ms ease-in-out;
    border: 3px solid white;
    margin: 20px 0;
    position: relative;

    &:hover {
      transform: translateY(3px);
    }
  }
}

@media screen and (max-width: 360px) {
  .card {
    min-width: 240px;
    width: 280px;
  }
}
</style>
