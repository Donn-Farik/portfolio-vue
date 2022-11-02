<script setup>
import { RouterView } from "vue-router";
import { ref } from "vue";
import navBar from "./components/navBar.vue";
import About from "./components/About.vue";
import { VueElement } from "@vue/runtime-dom";
import Hero from "./components/Hero.vue";
import Footer from "./components/Footer.vue";
import Skils from "./components/Skils.vue";
import Contact from "./components/Contact.vue";
import Cards from "./components/Cards.vue";
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

      <Skils />
      <div class="getColor">
        <h1 class="project">My projects</h1>
        <Cards
          image="https://ballesterockmusicdotcom.files.wordpress.com/2016/04/the-doors-logo.jpeg?w=640"
          title="Chat application"
          lorem="praesentium consequuntur saepe illo cumque nulla
      maxime doloribus hic quae. Itaque labore fugit, necessitatibus eaque
      beatae consequuntur nostrum similique reiciendis sit explicabo sed"
        />
        <Cards
          image="https://ballesterockmusicdotcom.files.wordpress.com/2016/04/the-doors-logo.jpeg?w=640"
          title="Todo App"
          lorem="praesentium consequuntur saepe illo cumque nulla
      maxime doloribus hic quae. Itaque labore fugit, necessitatibus eaque
      beatae consequuntur nostrum similique reiciendis sit explicabo sed"
        />
        <Cards
          image="https://ballesterockmusicdotcom.files.wordpress.com/2016/04/the-doors-logo.jpeg?w=640"
          title="spotify landing page"
          lorem="praesentium consequuntur saepe illo cumque nulla
      maxime doloribus hic quae. Itaque labore fugit, necessitatibus eaque
      beatae consequuntur nostrum similique reiciendis sit explicabo sed"
        />
        <Cards
          image="https://ballesterockmusicdotcom.files.wordpress.com/2016/04/the-doors-logo.jpeg?w=640"
          title="recipe website"
          lorem="praesentium consequuntur saepe illo cumque nulla
      maxime doloribus hic quae. Itaque labore fugit, necessitatibus eaque
      beatae consequuntur nostrum similique reiciendis sit explicabo sed"
        />
      </div>

      <Contact />
      <Footer />
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

  .navToggle {
    display: none;
  }
  .getColor {
    background-color: #2b2b2b;
  }
  .project {
    padding: 20px 0 1px 0;
    text-align: center;
    color: #ffe0b2;
  }
}
</style>
