<template>
  <div class="container">
    <v-card class="mx-auto fromCss" max-width="344">
      <img :src="props.image" />

      <v-card-title> {{ title }}</v-card-title>

      <v-card-subtitle> {{ lorem }} </v-card-subtitle>

      <v-card-actions>
        <v-btn color="orange lighten-2" text> Explore </v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script setup>
const props = defineProps({
  image: {
    type: String,
  },
  title: {
    type: String,
  },
  lorem: {
    type: String,
  },
});
</script>

<style scoped>
@media screen and (max-width: 992px) {
  .container {
    padding: 20px;
    /* height: 300px; */
  }
  h1 {
    margin-top: 13px;
    color: #ffe0b2;
  }
  .fromCss {
    margin-top: 30px;
  }
}
</style>
