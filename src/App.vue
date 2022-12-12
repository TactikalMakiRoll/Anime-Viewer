<template>
  <home-page></home-page>
</template>

<script setup>
import HomePage from "./pages/HomePage.vue"
</script>

<style>
/* Adding needed Netflix fonts */
@font-face {
  font-family: "Netflix Sans";
  src: url(../fonts/Netflix\ Sans\ Medium.otf) format("opentype");
}

@font-face {
  font-family: "Netflix Sans";
  src: url(../fonts/Netflix\ Sans\ Bold.otf) format("opentype");
  font-weight: bold;
}

@font-face {
  font-family: "Netflix Sans";
  src: url(../fonts/Netflix\ Sans\ Light.otf) format("opentype");
  font-weight: 300;
}

</style>
