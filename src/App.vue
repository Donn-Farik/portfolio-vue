<script setup>
import { RouterView } from "vue-router";
import { ref } from "vue";
import navBar from "./components/navBar.vue";
import About from "./components/About.vue";
import { VueElement } from "@vue/runtime-dom";
import Hero from "./components/Hero.vue";

const isActivated = ref(true);
const handleClick = () => {
  isActivated.value = !isActivated.value;
};
</script>
<template>
  <navBar @handleToggle="handleClick" />
  <!-- menu bar mobile first -->
  <div class="container">
    <nav :class="{ navToggle: isActivated }" class="navLinks">
      <a href="https://www.w3schools.com" target="_blank">Home</a>
      <a href="https://www.w3schools.com" target="_blank">About</a>
      <a href="https://www.w3schools.com" target="_blank">Portfolio</a>
      <a href="https://www.w3schools.com" target="_blank">Contact</a>
    </nav>
    <div class="todo">
      <Hero />
      <About />
    </div>
  </div>

  <RouterView />
</template>

<style scoped>
.navLinks {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #212121;
}
.navLinks a {
  text-decoration-line: none;
  padding: 30px;
  font-size: 1.5rem;
  color: whitesmoke;
  display: none;
}
.navLinks a:hover {
  color: #ffe0b2;
}
@media screen and (max-width: 992px) {
  .navLinks a {
    display: block;
    margin-top: 70px;
  }
  .navLinks {
    height: 753px;
  }

  .alooo {
    color: red;
  }

  .navToggle {
    display: none;
  }
  .todo {
    position: relative;
  }
}
</style>
