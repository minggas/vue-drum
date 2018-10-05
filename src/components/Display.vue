<template>
  <div class="display">
      <span>{{sound}}</span>
  </div>
</template>

<script>
export default {
  name: "Display",
  props: {
    sound: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.display {
  text-align: center;
  height: 6%;
  width: 10rem;
  margin: 0 auto;
  background: hsl(200, 4%, 49%);
  border: 3px inset hsl(203, 40%, 10%);
  border-radius: 5px;
  padding-top: 5px;
}
</style>
