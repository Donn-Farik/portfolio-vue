<template>
  <div class="container">
    <nav class="nav-links">
      <a href="https://www.w3schools.com" target="_blank">Home</a>
      <a href="https://www.w3schools.com" target="_blank">About</a>
      <a href="https://www.w3schools.com" target="_blank">Portfolio</a>
      <a href="https://www.w3schools.com" target="_blank">Contact</a>
    </nav>
  </div>
</template>

<script setup>
import { RouterLink } from "vue-router";
</script>

<style scoped>
.nav-links a {
  text-decoration-line: none;
  margin-left: 10rem;
  font-size: 1rem;
  font-family: "Roboto", sans-serif;
  font-size: 17px;
  color: white;
}

.nav-links a:hover {
  color: #ffe0b2;
}
@media screen and (max-width: 992px) {
  .nav-links a {
    display: none;
  }
}
</style>
