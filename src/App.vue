<template>
  <div id="app">
    <ApplicationBlock />
  </div>
</template>

<script>
import ApplicationBlock from "./components/ApplicationBlock.vue";
export default {
  name: "App",
  components: {
    ApplicationBlock,
  },
};
</script>

<style>
body {
  background: hsl(0, 0%, 90%);
  padding: 0;
  margin: 0;
  width: 100%;
  height: 100%;
  position: relative;
}
#app {
  overflow: hidden;
}
</style>
