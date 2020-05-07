<template>
  <section>
    <h2 class="sectionHeader">My projects</h2>
    <div>
      <card
        v-for="(content, index) in cardContent"
        :key="index"
        :name="content.name"
        :image="content.image"
        :dSmall="content.dSmall"
        :description="content.description"
        :dTwo="content.dTwo"
        :sourceLink="content.sourceLink"
        :activeLink="content.activeLink"
      ></card>
    </div>
  </section>
</template>

<script>
import card from "./Card.vue";
export default {
  components: {
    card: card
  },
  data() {
    return {
      cardContent: [
        {
          id: "1",
          name: "Water Commercial",
          dSmall: "School commercial project",
          image: require("@/assets/commercial.jpeg"),
          description:
            "I was given the freedom to chose the subject and make a 20 sec commercial about it, I wasn't alone, we chose to do a video commercial about water and it's importance in our daily life.",
          dTwo:
            "I took the roles of main actor and director, and the focus was to communicate how important water is out everyday life, how it is part of all of our activities from dusk till dawn.",
          sourceLink: "https://www.youtube.com/watch?v=5NYV_mr4IfM",
          activeLink: "https://www.youtube.com/watch?v=5NYV_mr4IfM"
        },
        {
          id: "2",
          name: "EASV Canteen website",
          dSmall: "Communcication inteface",
          image: require("@/assets/EASV-canteen-project.jpeg"),
          description:
            "After evaluating the EASV Canteen and talking to the customers we found that the biggest pains are long ques and lack of information, it became clear that it was lacking a communication portal.",
          dTwo:
            "To resolve this we set on designing a communication interface, especially for mobile and tablet use. The goal was to inform and create a community around food and cultural diversity  The following project is the result of that.",
          sourceLink: "https://github.com/raul-octavian/canteen-project",
          activeLink: "https://easvcanteen.netlify.app/"
        },
        {
          id: "3",
          name: "ToDo list from API",
          dSmall: "Using vuex to manipulate a public API",
          image: require("@/assets/todoList.jpg"),
          description:
            "The goal of this project was to learn how to use API's and Vuex state management pattern and to understand the logic behind it. ",
          dTwo:
            "I focused on the logic and operations so making it pretty was outside the scope. The todos are imported from a public JSON library and, the page offers the add, filter, delete and complete or incomplete state change on double-click.",
          sourceLink: "https://github.com/raul-octavian/vuex-and-api-totolist",
          activeLink: "https://raultodoapi.netlify.app/"
        },
        {
          id: "4",
          name: "Corona Video",
          dSmall: "School infomercial video",
          image: require("@/assets/corona.jpg"),
          description:
            "As a school team project, which allowed us to chose our subject, gave us the freedom and we chose to focus on the Corona pandemic from a quarantines person's perspective.",
          dTwo:
            "In this project, my role was as an animator and main actor. It was a pleasure to work with my colleagues and create something that is more than just a simple infomercial.",
          sourceLink: "https://www.youtube.com/watch?v=T5vAHnADXMY&t",
          activeLink: "https://www.youtube.com/watch?v=T5vAHnADXMY&t"
        }
      ]
    };
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