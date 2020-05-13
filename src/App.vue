<template>
  <div id="app">
    <Header />
    <Cube />
  </div>
</template>

<script>
import Header from "./components/layouts/Header";
import Cube from "./components/Cube.vue";
export default {
  name: "App",
  components: {
    Header,
    Cube
  }
};
</script>

<style>
body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}
</style>
