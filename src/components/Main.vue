<template>
  <div class="Main">
    <Nav />
    <h1>{{ msg }}</h1>
    <PhotoHolder />
  </div>
</template>

<script>
import Nav from "./Nav";
import PhotoHolder from "./PhotoHolder";

export default {
  name: "Main",
  components: {
    Nav,
    PhotoHolder
  },
  props: {
    msg: String
  }
};
</script>

<style scoped>
.Main {
  display: flex;
  flex-direction: column;
  align-content: center;
  width: 1000px;
  color: black;
  padding-bottom: 100px;
}
</style>
