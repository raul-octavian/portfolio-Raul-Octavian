<template>
  <form class="shadow contact-form">
    <section>
      <input
        type="text"
        name="user_name"
        id="name"
        class="input-fields"
        placeholder="your name"
        required
      />

      <input
        type="email"
        name="email"
        id="user_email"
        class="input-fields"
        placeholder="email"
        required
      />
    </section>
    <section>
      <textarea class="input-fields" name="message" id="textarea" placeholder="enter message here"></textarea>
    </section>
    <input type="submit" value="Send" id="submit" />
    <socialButtons></socialButtons>
  </form>
</template>

<script>
import emailjs from "emailjs-com";
import socialButtons from "./social-button.vue";
export default {
  components: {
    socialButtons: socialButtons
  },
  methods: {
    sendEmail: e => {
      emailjs
        .sendForm(
          "gmail",
          "template_7JzIFxzP",
          e.target,
          "user_LUUEYiIRn5R6Bw8Fwtxmu"
        )
        .then(
          result => {
            alert(
              "You succesfully submited your message",
              result.status,
              result.text
            );
          },
          error => {
            alert("The form failed to send, please try again", error);
          }
        );
    }
  }
};
</script>

<style lang="scss" scoped >
form {
  flex-grow: 1;
  background-color: $Gravity---Sand-Creatures-II-3-rgba;
  padding: 40px;
  width: 40%;
  margin-left: -1px;
}
textarea {
  width: calc(80% + 40px);
  min-height: 30vh;
}

input {
  width: 40%;
}

.input-fields {
  border-bottom: 2px solid $Gravity---Sand-Creatures-II-4-rgba;
  margin: 20px;
  padding: 10px 10px;
  font-size: $font-size-normal-mobile;
  color: $Gravity---Sand-Creatures-II-5-rgba;
  &:hover {
    border-bottom: 2px solid $Gravity---Sand-Creatures-II-5-rgba;
  }
  &::placeholder {
    color: $Gravity---Sand-Creatures-II-4-rgba;
  }
  &:focus,
  &:focus-visible,
  &:visited,
  &:active {
    color: $Gravity---Sand-Creatures-II-4-rgba;
    border-bottom: 2px solid $Gravity---Sand-Creatures-II-5-rgba;
  }
}
input:-webkit-autofill,
input:-webkit-autofill:hover,
input:-webkit-autofill:focus,
input:-webkit-autofill:active {
  -webkit-animation: autofill 0s forwards;
  animation: autofill 0s forwards;
}

@keyframes autofill {
  100% {
    background: transparent;
    color: $Gravity---Sand-Creatures-II-5-rgba;
    border-bottom: 2px solid $Gravity---Sand-Creatures-II-5-rgba;
  }
}

@-webkit-keyframes autofill {
  100% {
    background: transparent;
    color: $Gravity---Sand-Creatures-II-5-rgba;
    border-bottom: 2px solid $Gravity---Sand-Creatures-II-5-rgba;
  }
}

#submit {
  padding: 10px 50px;
  background-color: $Gravity---Sand-Creatures-II-1-rgba;
  border-radius: 30px;
  text-transform: uppercase;
  font-family: "Fira Sans", sans-serif;
  margin: 20px;
  font-weight: 600;
  width: auto;
}

@media screen and (max-width: 1200px) {
  input {
    width: 100%;
  }
  textarea {
    width: 100%;
    min-height: 20vh;
  }
}

@media screen and (max-width: 960px) {
  form {
    flex-grow: 2;
  }
  .input-fields,
  #submit {
    margin-left: 0;
  }
}
</style>