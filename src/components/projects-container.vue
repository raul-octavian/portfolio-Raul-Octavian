<template>
  <section>
    <h2 class="sectionHeader">My projects</h2>
    <div>
      <card></card>
      <card></card>
      <card></card>
    </div>
  </section>
</template>

<script>
import card from "./Card.vue";
export default {
  components: {
    card: card
  }
};
</script>

<style lang="scss" scoped>
section {
  height: 100%;
}

h2 {
  color: $Gravity---Sand-Creatures-II-3-rgba;
}

div {
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;
}
</style>