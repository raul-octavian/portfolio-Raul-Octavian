<template>
  <article class="shadow">
    <a href="#">
      <div class="img-container">
        <div class="project-image"></div>
        <h4>name of project</h4>
      </div>
      <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
      <a class="flex">
        <button class="read-more">Read more</button>
      </a>
    </a>
  </article>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
article {
  height: 500px;
  width: 350px;
  background: $Gravity---Sand-Creatures-II-5-rgba;
  padding: 20px 40px;
  transition: all 500ms ease-in-out;
  border: 3px solid white;
  margin: 20px;

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
}
.project-image {
  background: url("../assets/mobile first responsive app.png");
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
}

@media screen and (max-width: 600px) {
  article {
    height: 430px;
    width: 320px;
    background: $Gravity---Sand-Creatures-II-5-rgba;
    padding: 20px 10px;
    transition: all 500ms ease-in-out;
    border: 2px solid white;
    margin: none;
  }
}
</style>