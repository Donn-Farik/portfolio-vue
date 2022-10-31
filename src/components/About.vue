<template>
  <div class="container">
    <h1 class="title total">About Me</h1>
    <img
      src="../Image/280201098_10229195915903150_2101689533609127444_n.jpg"
      alt=""
      class="circular-square"
    />
    <p class="text total">
      I'm a web developer with a focus on Javascript and Vue.js , but still
      exploring other technologies and frameworks that catch my interest! if
      you're looking for a developer to add to your team,I'd love to hear from
      you!
    </p>
  </div>
</template>

<script setup></script>

<style scoped>
.container {
  background-color: #2b2b2b;
  /* height: 400px; */
}
.total {
  padding: 30px;
}
.title {
  color: #ffe0b2;
}
.text {
  color: #e7e7e7;
  font-size: 19px;
}
.circular-square {
  border-top-left-radius: 50% 50%;
  border-top-right-radius: 50% 50%;
  border-bottom-right-radius: 50% 50%;
  border-bottom-left-radius: 50% 50%;
  height: 200px;
  width: 200px;
  margin: 40px 0px 40px 100px;
}
</style>
