<template>
  <div class="full-width">
    <h2 class="sectionHeader">My life in images</h2>
    <section id="image-container">
      <imageCoffeShop></imageCoffeShop>
      <imageRabit></imageRabit>
      <imageAtHome></imageAtHome>
      <imageVienna></imageVienna>
    </section>
  </div>
</template>

<script>
import imageCoffeShop from "./image-coffe-shop.vue";
import imagerabit from "./image-rabit";
import imageAtHome from "./image-at-home";
import imageVienna from "./image-in-Vienna";
export default {
  components: {
    imageCoffeShop: imageCoffeShop,
    imageRabit: imagerabit,
    imageAtHome: imageAtHome,
    imageVienna: imageVienna
  }
};
</script>

<style lang="scss" scoped>
.full-width {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
#image-container {
  display: flex;
  flex-wrap: wrap;
  flex-grow: 1;
  justify-content: space-around;
  align-items: center;
}
// @media only screen and (max-width: 650px) {
//   #image-container {
//     margin-top: 0;
//   }
// }

// @media only screen and (max-width: 980px) {
//   #image-container {
//     grid-template-columns: repeat(5, 70px);
//     grid-template-rows: repeat(5, 70px);
//     grid-template-areas:
//       "coffe coffe rabit rabit rabit"
//       "coffe coffe rabit rabit rabit"
//       "coffe coffe . vienna vienna"
//       "home home home vienna vienna"
//       "home home home vienna vienna";
//   }
// }

// @media only screen and (max-width: 600px) {
//   #image-container {
//     grid-template-columns: repeat(5, 50px);
//     grid-template-rows: repeat(6, 50px);
//   }
// }

// @media only screen and (max-width: 490px) {
//   #image-container {
//     padding-right: 20px;
//     grid-template-columns: repeat(2, 45%);
//     grid-template-rows: repeat(5, 50px);
//     grid-gap: 20px;
//     width: 100%;
//     grid-template-areas:
//       "coffe vienna "
//       "coffe vienna "
//       "coffe vienna "
//       "home rabit "
//       "home rabit ";
//   }
// }

// @media only screen and (max-width: 570px) {
//   h2 {
//     font-size: $font-size-medium-tablet;
//   }
// }

// @media only screen and (max-width: 490px) {
//   h2 {
//     font-size: $font-size-medium-mobile;
//   }
//   #image-container {
//     padding-right: 20px;
//     grid-template-columns: repeat(2, 45%);
//     grid-template-rows: repeat(6, 50px);
//     grid-gap: 10px;
//   }
// }
</style>