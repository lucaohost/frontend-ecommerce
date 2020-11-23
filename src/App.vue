<template>
  <div id="app">
    <Ecommerce msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import Ecommerce from "./components/Ecommerce.vue";

export default {
  name: "App",
  components: {
    Ecommerce,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css family=Titillium+Web:300,400,400i,600,600i,700");
#app {
  font-family: "Titillium Web", Arial;
}
</style>

<style lang="scss">
@import "./css/general.scss";

body,
html {
  padding: 0;
  margin: 0;
  overflow-x: hidden;
}
* {
  box-sizing: border-box;
}
#app {
  min-height: 100vh;
}
</style>
