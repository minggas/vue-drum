/* eslint-disable */
<template>
  <div class="drum-pad" :data-key="keyId" @click="playSound">
    <kbd>{{btnKey}}</kbd>
    <span class="sound">{{pad}}</span>
    <audio :ref="keyId" :src="soundEnd" :id="pad"></audio>
  </div>
</template>

<script>
export default {
  name: "PadButton",
  props: {
    btnKey: String,
    keyId: String,
    pad: String,
    soundEnd: String
  },
  created: function() {
    window.addEventListener("keypress", this.playSound);
  },
  methods: {
    playSound: function(e) {
      const audio = this.$refs[e.keyCode || e.currentTarget.dataset.key];
      if (!audio) return;
      audio.currentTime = 0;
      audio.play();
      this.$parent.display = audio.id;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.drum-pad {
  cursor: pointer;
  min-width: 3rem;
  margin: 0.2rem;
  font-size: calc(0.3rem + 1vh);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  transition: all 0.07s;
  background-color: hsla(203, 25%, 74%, 0.7);
  border-radius: 10px;
  border: none;
  box-shadow: 0px 3px 0px 0px #222121, inset -1px -3px 10px 1px #515151;
}

.drum-pad kbd {
  font-size: calc(1rem + 2vw);
}
</style>
