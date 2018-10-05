<template>
  <div class="pad">
    <PadButton keyId="113" btnKey="Q" pad="Kick" soundEnd="/sounds/Kick.mp3"/>
    <PadButton keyId="119" btnKey="W" pad="HiHat" soundEnd="./sounds/HiHat.mp3"/>
    <PadButton keyId="101" btnKey="E" pad="Snare" soundEnd="./sounds/Snare.mp3"/>
    <PadButton keyId="97" btnKey="A" pad="Openhat" soundEnd="./sounds/Openhat.mp3"/>
    <PadButton keyId="115" btnKey="S" pad="TomFloor" soundEnd="./sounds/TomFloor.mp3"/>
    <PadButton keyId="100" btnKey="D" pad="TomMid" soundEnd="./sounds/TomMid.mp3"/>
    <PadButton keyId="122" btnKey="Z" pad="TomHigh" soundEnd="./sounds/TomHigh.mp3"/>
    <PadButton keyId="120" btnKey="X" pad="Crash" soundEnd="./sounds/Crash.mp3"/>
    <PadButton keyId="99" btnKey="C" pad="RideCymbal" soundEnd="./sounds/RideCymbal.mp3"/>
  </div>
</template>

<script>
import PadButton from "./PadButton.vue";

export default {
  name: "Pad",
  components: {
    PadButton
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.pad {
  height: 85%;
  padding: 2rem;
  grid-gap: 0.8rem;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(3, 1fr);
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
