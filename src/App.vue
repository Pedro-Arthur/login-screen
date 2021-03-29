<template>
  <div class="app">
    <Welcome />
    <Login />
  </div>
</template>

<script>
import Welcome from "./components/Welcome.vue";
import Login from "./components/Login.vue";

export default {
  name: "App",
  components: {
    Welcome,
    Login,
  },
};
</script>

<style scoped>
@font-face {
  font-family: InfraRegular;
  src: url(./assets/fonts/InfraRegular.woff);
}
@font-face {
  font-family: InfraLight;
  src: url(./assets/fonts/InfraLight.woff);
}
@font-face {
  font-family: InfraBold;
  src: url(./assets/fonts/InfraBold.woff);
}
.app {
  display: flex;
  font-family: InfraRegular;
}
</style>