<template>
  <!-- <img :src="{ imagen }" alt="imagen" /> -->
  <div class="container">
    <div class="hero-text">
      <h2 class="hero-title hero-color">HI THERE I'M</h2>
      <h1 class="hero-name hero-color">Fakhreddine Farik</h1>
      <P class="hero-text hero-color"
        >A Front-end web Developer passionate about creating interactive
        applications and experiences on the web.</P
      >
    </div>
  </div>
</template>

<script setup>
// props = defineProps({
//   imagen: {
//     type: String,
//   },
// });
</script>

<style scoped>
.container {
  background-color: #212121;
  height: 400px;
}
.hero-color {
  color: #e7e7e7;
  padding: 30px;
}
.hero-name {
  color: #ffe0b2;
}
.hero-text {
  font-size: 19px;
}
</style>
