<template>
  <main id="app">
    <logoHeader id="header"></logoHeader>
    <navigation></navigation>
    <section id="home">
      <herotext :textContent="textContent"></herotext>
      <heroImage></heroImage>
    </section>
    <section id="projects">
      <projectContainer></projectContainer>
    </section>

    <section id="about">
      <h2 class="sectionHeader">About me</h2>
      <div class="flex-container">
        <div class="elementContainer">
          <aboutText :textContent="textContent"></aboutText>
        </div>

        <div class="elementContainer">
          <videoCV></videoCV>
        </div>
      </div>
    </section>
    <section id="myPics">
      <imageContainer></imageContainer>
    </section>
    <section id="contact">
      <contact></contact>
    </section>

    <router-view />
  </main>
</template>

<script>
import logoHeader from "@/components/Header";
import aboutText from "@/components/About-text.vue";
import herotext from "@/components/Hero-top.vue";
import imageContainer from "@/components/image-container";
import projectContainer from "@/components/projects-container";
import contact from "@/components/contact";
import videoCV from "@/components/videoCV";
import heroImage from "@/components/Hero-container";
import navigation from "@/components/navigation";

export default {
  data() {
    return {
      textContent: {
        name: "Raul-Octavian Albu",
        activity: "front-end developer",
        heroOne: "The world is as we make it,",
        heroTwo: "and we are responsible to make it great.",
        heroThree: "I am a front-end developer in training,",
        heroFive: "the following content will show who I am,",
        heroSix: "my skills, priorities and make it ease for anyone",
        heroSeven: "to get to know me.",
        aboutTitle: "My core beliefes",
        aboutOne:
          "My INTJ-A aka “The Architect” personality and idealistic view of the world around me combined with optimistic nature push me towards achieving the impossible.",
        aboutTwo:
          "The idea of doing something half-way is very unsettling to me, I was raised with the belief that if you do not plan to do something right, then don’t do it at all.",
        aboutThree:
          "I consider life to be about learning and self-actualization, that's why I embarked on this journey so late in my life.",
        aboutFour:
          "I have so much to offer, so many dreams to fulfil, so many people to help."
      }
    };
  },

  components: {
    logoHeader: logoHeader,
    imageContainer: imageContainer,
    projectContainer: projectContainer,
    contact: contact,
    videoCV: videoCV,
    aboutText: aboutText,
    herotext: herotext,
    heroImage: heroImage,
    navigation: navigation
  }
};
</script>


<style lang="scss">
@import url("./styles/mixins.scss");
@import url("./styles/variables.scss");
@import url("https://fonts.googleapis.com/css?family=Barlow&display=swap");
@import url("https://fonts.googleapis.com/css?family=Fira+Sans:100,100i,200,200i,300,300i,400,400i,500,500i,600,600i,700,700i,800,800i,900,900i&display=swap&subset=latin-ext");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  color: $Gravity---Sand-Creatures-II-2-rgba;
  outline: none;
}
#app {
  font-family: "Fira Sans", sans-serif;
}

#home,
#myPics {
  min-height: 100vh;
  background: $Gravity---Sand-Creatures-II-2-rgba;
  padding: 0 15vw 10vh;
}

#projects {
  min-height: 100vh;
  padding: 0 15vw 10vh;
  background-color: $Gravity---Sand-Creatures-II-4-rgba;
}

#home {
  position: relative;
  display: flex;
  flex-direction: row;
}

#about,
#contact {
  background-color: $Gravity---Sand-Creatures-II-3-rgba;
  min-height: 100vh;
  padding-bottom: 10vh;
  padding: 0 15vw 10vh;
}

#contact {
  display: flex;
  justify-content: center;
  flex-direction: column;
  background-color: $Gravity---Sand-Creatures-II-4-hsla;
}
.sectionHeader {
  text-align: center;
  padding: 80px 0;
  font-weight: 700;
  color: $Gravity---Sand-Creatures-II-1-rgba;
}

.flex-container {
  display: flex;
  justify-content: space-around;
  align-items: center;
  min-height: 65vh;
}
.elementContainer {
  max-width: 50%;
  width: 45%;
  height: 100%;
  margin: 20px;
  &:nth-child(odd) {
    margin-left: 0;
  }
  &:nth-child(even) {
    margin-right: 0;
  }
}
// image display and general format
.imageDisplay {
  width: 250px;
  height: 300px;
  border: 3px solid white;
  margin-bottom: 5px;
}
.figCaption {
  text-align: right;
  font-style: italic;
  font-size: 10px;
  color: $Gravity---Sand-Creatures-II-5-rgba;
}
.pictureElement {
  position: relative;
  padding-bottom: 10px;
  margin: 10px 10px 200px;
  transform-origin: center;
  transform: perspective(800px) rotateY(10deg);
  transition: 0.5s;
  -webkit-box-reflect: below 1px
    linear-gradient(transparent, transparent, #0004);

  &:hover {
    transform: perspective(800px) rotateY(0deg);
    opacity: 1;
  }
}
// font-size styling for the hole website
.sectionHeader {
  font-size: $font-size-xlarge;
}
h1 {
  font-size: $font-size-large;
}
h2 {
  font-size: $font-size-medium;
}
h3 {
  font-size: $font-size-medium;
}
.about-text {
  font-size: $font-size-small;
}
#top-one-text,
#top-two-text {
  font-size: $font-size-normal;
}
h4 {
  font-size: $font-size-normal;
}
p {
  font-size: $font-size-small;
}

@media screen and (max-width: 1200px) {
  .sectionHeader {
    font-size: $font-size-large;
  }
}

@media screen and (max-width: 1200px) {
  .flex-container {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    min-height: 65vh;
  }
  .elementContainer {
    max-width: 100%;
    width: 100%;
    height: auto;
    margin: 20px;
    &:nth-child(odd) {
      margin-left: 20px;
    }
    &:nth-child(even) {
      margin-right: 20px;
    }
  }
}
@media screen and (max-width: 1100px) {
  .sectionHeader {
    font-size: $font-size-xlarge-tablet;
  }
  h1 {
    font-size: $font-size-xlarge-tablet;
  }
  #home,
  #myPics {
    padding: 0 20vw 10vh;
  }

  #projects {
    padding: 0 20vw 10vh;
  }

  #about,
  #contact {
    padding: 0 20vw 10vh;
  }
}

@media screen and (max-width: 960px) {
  #home {
    padding-top: calc(10vh + 80px);
  }
  .sectionHeader {
    font-size: $font-size-large-tablet;
  }
  h1 {
    font-size: $font-size-large-tablet;
  }
  h2 {
    font-size: $font-size-large-tablet;
  }
  h3 {
    font-size: $font-size-medium-tablet;
  }
  h4 {
    font-size: $font-size-normal-tablet;
  }
  p {
    font-size: $font-size-normal-mobile;
  }
  #top-one-text,
  #top-two-text {
    font-size: $font-size-medium-mobile;
  }
  .about-text {
    font-size: $font-size-normal-tablet;
  }
  .pictureElement {
    transform: perspective(800px) rotateY(0deg);
    transition: 0.5s;
    -webkit-box-reflect: below 1px
      linear-gradient(transparent, transparent, #0004);

    &:hover {
      transform: perspective(800px) scale(1.02);
    }
  }
}

@media screen and (max-width: 600px) {
  .sectionHeader {
    font-size: $font-size-xlarge-mobile;
  }
  h1 {
    font-size: $font-size-large-mobile;
  }
  h2 {
    font-size: $font-size-medium-mobile;
  }
  h3 {
    font-size: $font-size-medium-mobile;
  }
  h4 {
    font-size: $font-size-normal-mobile;
  }
  p {
    font-size: $font-size-normal-mobile;
  }
  #top-one-text,
  #top-two-text {
    font-size: $font-size-normal-mobile;
  }
  .about-text {
    font-size: $font-size-normal-mobile;
  }
  #home,
  #myPics {
    padding: 10vh 5vw 10vh;
    min-height: 80vh;
  }
  #home {
    padding-top: calc(10vh + 80px);
  }

  #projects {
    padding: 10vh 5vw 10vh;
    min-height: 80vh;
  }

  #about,
  #contact {
    padding: 10vh 5vw 10vh;
    min-height: 80vh;
  }
}

@media screen and (max-width: 350px) {
  .sectionHeader {
    font-size: $font-size-large-mobile;
  }
  h1 {
    font-size: $font-size-large-mobile;
  }
}
</style>
