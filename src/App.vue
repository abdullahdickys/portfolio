<script type="text/javascript">
import NavBar from "@/components/NavBar.vue";
export default {
  components: {
    NavBar, // register component
  },
};
</script>

<template>
  <div id="app">
    <NavBar />
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
  scroll-behavior: smooth;
}
</style>
