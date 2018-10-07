<template>
  <div id="app">
    <Title title="Virtual Drum" />
    <Display v-bind:sound="display" />       
    <div class="pad">
      <PadButton keyId="113" btnKey="Q" pad="Kick" soundEnd="/sounds/Kick.mp3" @click="this.display = 'Kick'"/>
      <PadButton keyId="119" btnKey="W" pad="HiHat" soundEnd="./sounds/HiHat.mp3"/>
      <PadButton keyId="101" btnKey="E" pad="Snare" soundEnd="./sounds/Snare.mp3"/>
      <PadButton keyId="97" btnKey="A" pad="Openhat" soundEnd="./sounds/Openhat.mp3"/>
      <PadButton keyId="115" btnKey="S" pad="TomFloor" soundEnd="./sounds/TomFloor.mp3"/>
      <PadButton keyId="100" btnKey="D" pad="TomMid" soundEnd="./sounds/TomMid.mp3"/>
      <PadButton keyId="122" btnKey="Z" pad="TomHigh" soundEnd="./sounds/TomHigh.mp3"/>
      <PadButton keyId="120" btnKey="X" pad="Crash" soundEnd="./sounds/Crash.mp3"/>
      <PadButton keyId="99" btnKey="C" pad="RideCymbal" soundEnd="./sounds/RideCymbal.mp3"/>
  </div>
  </div>
</template>

<script>
import PadButton from "./components/PadButton.vue";
import Title from "./components/Title.vue";
import Display from "./components/Display.vue";

export default {
  name: "app",
  components: {
    PadButton,
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
