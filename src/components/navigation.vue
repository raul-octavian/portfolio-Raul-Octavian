<template>
  <nav id="navigation">
    <home></home>
    <projects></projects>
    <about></about>
    <contact></contact>
  </nav>
</template>

<script>
import home from "@/components/nav-element-home";
import projects from "@/components/nav-element-projects";
import about from "@/components/nav-element-about";
import contact from "@/components/nav-element-contact";
export default {
  components: {
    home: home,
    projects: projects,
    about: about,
    contact: contact
  }
};
</script>

<style lang="scss">
//positioning the element

#navigation {
  position: fixed;
  top: 60px;
  z-index: 10;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.nav-element {
  position: absolute;
  left: -70px;
  z-index: 10;
  transition: all 300ms ease-in-out;

  &:hover {
    left: 0px;
  }
}

// styleing element
.nav-element {
  max-width: 110px;
  padding: 30px 0 30px 20px;
  display: flex;
  justify-content: flex-end;
  border: 2px solid $Gravity---Sand-Creatures-II-1-rgba;
  border-right: none;
  border-left: none;
  margin: 30px 0;
  position: relative;
  background: $Gravity---Sand-Creatures-II-2-rgba;
  z-index: 90;

  &:before {
    content: "";
    height: 70px;
    width: 70px;
    border: 2px solid $Gravity---Sand-Creatures-II-1-rgba;
    background: $Gravity---Sand-Creatures-II-2-rgba;
    z-index: 89;
    border-bottom: none;
    border-left: none;
    border-radius: 0 10px 0 0;
    position: absolute;
    right: -32%;
    top: 12px;
    transform: rotateZ(45deg);
  }

  svg {
    height: 30px;
    width: 40px;
    margin-left: 20px;
    margin-right: -20px;
    z-index: 90;
    position: relative;
  }
}
svg {
  height: 30px;
}
.cls-1 {
  fill: #f0e4d9;
}

.navigation-link {
  text-decoration: none;
  text-transform: uppercase;
  position: relative;
  z-index: 90;
  p {
    font-size: $font-size-normal-mobile;
    line-height: 30px;
    color: $Gravity---Sand-Creatures-II-1-rgba;
    z-index: 90;
    position: relative;
  }
}
@media screen and (max-width: 600px) {
  #navigation {
    position: fixed;
    top: 80px;
    z-index: 90;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    width: 100%;
  }
  //position change
  .nav-element {
    position: absolute;
    left: 0px;
    top: -35px;
    z-index: 90;
    transition: all 300ms ease-in-out;

    &:hover {
      left: 0px;
      top: 0px;
    }
  }

  // styleing element
  .nav-element {
    width: 80px;
    height: 70px;
    padding: 0 10px;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;
    border: 2px solid $Gravity---Sand-Creatures-II-1-rgba;
    border-right: 2px solid $Gravity---Sand-Creatures-II-1-rgba;
    border-left: 2px solid $Gravity---Sand-Creatures-II-1-rgba;
    border-radius: 0 0 8px 8px;
    border-top: none;
    border-bottom: none;
    margin: 0 0;
    position: relative;
    background: $Gravity---Sand-Creatures-II-2-rgba;
    z-index: 90;

    &:before {
      content: "";
      height: 55px;
      width: 55px;
      border: 2px solid $Gravity---Sand-Creatures-II-1-rgba;
      background: $Gravity---Sand-Creatures-II-2-rgba;
      z-index: 89;
      border-bottom: none;
      border-left: none;
      border-radius: 0 10px 0 0;
      position: absolute;
      right: 11px;
      top: 55%;

      transform: rotateZ(135deg);
    }
    svg {
      height: 30px;
      width: 40px;
      margin-left: 0;
      margin-right: 0;
      margin-top: 10px;
      margin-bottom: -15px;
      z-index: 90;
      position: relative;
    }
  }
  .navigation-link {
    p {
      text-align: center;
    }
  }
}
</style>