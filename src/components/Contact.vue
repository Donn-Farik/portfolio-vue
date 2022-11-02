<template>
  <div class="container">
    <h1>Contact Me</h1>
    <form action="" class="form-section">
      <!-- <label for="">Your Name</label>
      <input type="text" />
      <label for="">Your email</label>
      <input type="email" />
      <label for="">would you write somthing?</label>
      <textarea name="" id="" cols="30" rows="10"></textarea> -->
      <v-text-field
        v-model="firstname"
        :counter="10"
        label="Your Name"
        class="input"
        required
      ></v-text-field>
      <v-text-field
        v-model="email"
        :rules="emailRules"
        label="E-mail"
        class="input"
        required
      ></v-text-field>
      <v-textarea
        clearable
        clear-icon="mdi-close-circle"
        label="would you write somthing ?"
        class="textArea"
      ></v-textarea>

      <v-btn class="btn" block elevation="14" x-large>Get in touch</v-btn>
    </form>

    <div class="footer">
      <a href="">Linkiding</a>
      <a href="">Tweeter</a>
      <h3>Created & designed by Fakhreddine Farik</h3>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
@media screen and (max-width: 992px) {
  .container {
    background-color: #212121;
    padding: 30px;
    color: aliceblue;
  }
  h1 {
    text-align: center;
    color: #ffe0b2;
    padding-bottom: 50px;
  }
  .btn {
    color: #212121;
  }
  .btn:hover {
    background-color: #ffe0b2;
  }
}
</style>
