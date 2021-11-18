<template>
  <div id="app">
    <div class="alert alert-success" role="alert">
      Microfrontend Calculadora
    </div>

    <Calculadora />
  </div>
</template>

<script>
import Calculadora from "@/components/Calculadora.vue";

export default {
  name: "App",
  components: {
    Calculadora,
  }
};
</script>

<style lang="scss">
@import "https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css";

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
