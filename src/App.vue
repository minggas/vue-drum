<template>
  <div id="app">
    <Title title="Virtual Drum" />
    <Display sound="teste" />       
    <Pad />
  </div>
</template>

<script>
import Pad from "./components/Pad.vue";
import Title from "./components/Title.vue";
import Display from "./components/Display.vue";

export default {
  name: "app",
  components: {
    Pad,
    Title,
    Display
  }
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  font-family: Arial, Helvetica, sans-serif;
  background: hsl(173, 30%, 20%);
}
body {
  width: 100vw;
  height: 100vh;
  padding: 8vh 10vw;
}

#app {
  width: 100%;
  height: 100%;
  background-color: hsl(203, 21%, 20%);
  border: 2px solid hsl(203, 40%, 10%);
  border-radius: 15px;
  box-shadow: 7px 10px 34px 1px rgba(0, 0, 0, 0.68), inset -1px -6px 12px;
}
</style>
