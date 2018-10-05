<template>
  <div class="title">
      <h1>{{title}}</h1>
  </div>
</template>

<script>
export default {
  name: "Title",
  props: {
    title: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.title {
  height: 10%;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 2%;
  color: hsl(203, 0%, 36%);
  font-size: calc(0.5rem + 1vh);
  font-weight: 700;
  letter-spacing: 1rem;
}
</style>
