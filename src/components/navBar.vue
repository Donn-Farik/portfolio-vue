<template>
  <div class="wrapper">
    <div class="logo">Farik</div>
    <nav class="nav-links">
      <RouterLinks />
    </nav>
    <v-app-bar-nav-icon
      class="menu-bar"
      @click="$emit('handleToggle')"
    ></v-app-bar-nav-icon>
  </div>
</template>

<script setup>
import { RouterLink } from "vue-router";
import RouterLinks from "./RouterLinks.vue";

const emit = defineEmits(["handleToggle"]);
// const handleToggle = () => {
//   emit("pipa");
// };
</script>

<style scoped>
.menu-bar {
  display: none;
  color: azure;
  background-color: #212121;
  margin-left: 300px;
}
.wrapper {
  position: relative;
  display: flex;
  justify-content: space-around;
  align-items: center;
  background-color: #212121;
  padding: 2rem 0 2rem 0;
}

.logo {
  position: absolute;
  left: 50px;
  font-family: "Pacifico", cursive;
  font-weight: 400;
  color: #ffe0b2;
  font-size: 1.5rem;
}
@media screen and (max-width: 992px) {
  .menu-bar {
    display: block;
    cursor: pointer;
    width: 300px;
  }

  .wrapper {
    padding: 1.5rem;
  }
}
</style>
