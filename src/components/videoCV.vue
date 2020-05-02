.<template>
  <section id="video">
    <iframe
      height="315"
      width="520"
      src="https://www.youtube.com/embed/X9HCTMetvKc"
      frameborder="0"
      allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen
    ></iframe>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
#video {
  display: flex;
  justify-content: center;
  background-color: $Gravity---Sand-Creatures-II-2-rgba;
  padding: 40px;
  height: 65vh;
  min-height: 65vh;
}
iframe {
  max-width: 100%;
  max-height: 100%;
  width: 100%;
  height: 100%;
}
</style>