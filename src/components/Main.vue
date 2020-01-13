<template>
  <div class="Main">
    <Nav v-on:getDate="onClick" />
    <PhotoHolder v-bind:date="date" />
  </div>
</template>

<script>
import Nav from "./Nav";
import PhotoHolder from "./PhotoHolder";

export default {
  name: "Main",
  data() {
    return {
      date: null
    };
  },
  components: {
    Nav,
    PhotoHolder
  },
  methods: {
    onClick(newDate) {
      this.date = newDate;
    }
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
