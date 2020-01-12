<template>
  <div id="app">
    <Main msg="Hello World" />
  </div>
</template>

<script>
import Main from "./components/Main";

export default {
  name: "app",
  components: {
    Main
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: black;
}

body {
  background: black;
  display: flex;
  flex-direction: column;
  align-items: center;
}

* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}
</style>
