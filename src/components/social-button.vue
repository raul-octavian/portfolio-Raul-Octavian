<template>
  <section>
    <div class="container">
      <a href="https://www.linkedin.com/in/raul-octavian-albu" target="blank">
        <div class="element-social">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 447.98">
            <g id="Layer_2" data-name="Layer 2">
              <g id="Layer_1-2" data-name="Layer 1">
                <path
                  d="M100.28,448H7.4V148.88h92.88ZM53.79,108.08C24.09,108.08,0,83.48,0,53.78a53.79,53.79,0,0,1,107.58,0C107.58,83.48,83.48,108.08,53.79,108.08ZM447.9,448H355.22V302.38c0-34.7-.7-79.2-48.29-79.2-48.29,0-55.69,37.7-55.69,76.7V448H158.46V148.88h89.08v40.8h1.3c12.4-23.5,42.69-48.3,87.88-48.3,94,0,111.28,61.9,111.28,142.3V448Z"
                />
              </g>
            </g>
          </svg>
        </div>
      </a>
      <a href="https://github.com/raul-octavian" target="blank">
        <div class="element-social">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 496 483.61">
            <g id="Layer_2" data-name="Layer 2">
              <g id="Layer_1-2" data-name="Layer 1">
                <path
                  d="M165.9,389.4c0,2-2.3,3.6-5.2,3.6-3.3.3-5.6-1.3-5.6-3.6,0-2,2.3-3.6,5.2-3.6C163.3,385.5,165.9,387.1,165.9,389.4Zm-31.1-4.5c-.7,2,1.3,4.3,4.3,4.9,2.6,1,5.6,0,6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5.3-6.2,2.3Zm44.2-1.7c-2.9.7-4.9,2.6-4.6,4.9.3,2,2.9,3.3,5.9,2.6s4.9-2.6,4.6-4.6S181.9,382.9,179,383.2ZM244.8,0C106.1,0,0,105.3,0,244,0,354.9,69.8,449.8,169.5,483.2c12.8,2.3,17.3-5.6,17.3-12.1,0-6.2-.3-40.4-.3-61.4,0,0-70,15-84.7-29.8,0,0-11.4-29.1-27.8-36.6,0,0-22.9-15.7,1.6-15.4,0,0,24.9,2,38.6,25.8,21.9,38.6,58.6,27.5,72.9,20.9,2.3-16,8.8-27.1,16-33.7-55.9-6.2-112.3-14.3-112.3-110.5,0-27.5,7.6-41.3,23.6-58.9-2.6-6.5-11.1-33.3,2.6-67.9,20.9-6.5,69,27,69,27a236.24,236.24,0,0,1,125.6,0s48.1-33.6,69-27c13.7,34.7,5.2,61.4,2.6,67.9,16,17.7,25.8,31.5,25.8,58.9,0,96.5-58.9,104.2-114.8,110.5,9.2,7.9,17,22.9,17,46.4,0,33.7-.3,75.4-.3,83.6,0,6.5,4.6,14.4,17.3,12.1C428.2,449.8,496,354.9,496,244,496,105.3,383.5,0,244.8,0ZM97.2,344.9c-1.3,1-1,3.3.7,5.2,1.6,1.6,3.9,2.3,5.2,1,1.3-1,1-3.3-.7-5.2C100.8,344.3,98.5,343.6,97.2,344.9Zm-10.8-8.1c-.7,1.3.3,2.9,2.3,3.9,1.6,1,3.6.7,4.3-.7s-.3-2.9-2.3-3.9C88.7,335.5,87.1,335.8,86.4,336.8Zm32.4,35.6c-1.6,1.3-1,4.3,1.3,6.2,2.3,2.3,5.2,2.6,6.5,1,1.3-1.3.7-4.3-1.3-6.2C123.1,371.1,120.1,370.8,118.8,372.4Zm-11.4-14.7c-1.6,1-1.6,3.6,0,5.9s4.3,3.3,5.6,2.3c1.6-1.3,1.6-3.9,0-6.2-1.4-2.3-4-3.3-5.6-2Z"
                />
              </g>
            </g>
          </svg>
        </div>
      </a>
    </div>
  </section>
</template>


<script>
export default {};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  margin: 0;
  padding: 0;
  width: 20%;
  margin: 20px;
}
.element-social {
  min-width: 50px;
  min-height: 50px;
  margin: 0 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 50%;
  box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.05),
    -2px -2px 2px rgba(136, 168, 191, 0.5);
  position: relative;
  transform: all 200ms ease-in-out;
  &:first-child {
    margin-left: 0;
  }

  &:before {
    content: "";
    height: 80%;
    width: 80%;
    position: absolute;
    box-shadow: inset 2px 2px 2px rgba(0, 0, 0, 0.05),
      inset -2px -2px 2px rgba(136, 168, 191, 0.5);
    border-radius: 50%;
  }

  &:hover {
    box-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3),
      -1px -1px 3px rgba(17, 28, 38, 0.5);
  }
}

.fill-color {
  fill: $Gravity---Sand-Creatures-II-2-rgba;
}

svg {
  height: 20px;
  width: 20px;
}
</style>