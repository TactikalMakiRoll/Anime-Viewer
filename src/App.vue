<template>
  <login-page></login-page>
</template>

<script>
import LoginPage from "./pages/LoginPage.vue"

export default {
  name: "App",
  components:{
    LoginPage,
  }
};
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
  font-weight: lighter;
}

</style>
