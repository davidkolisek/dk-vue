<template>
  <div class="main-content">
      <router-view />
      <Navigation />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Navigation from "./components/layout/Navigation.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Navigation,
  },
};
</script>

<style lang="scss">
.main-content {
  width: 100%;
  height: 100%;
}
</style>
