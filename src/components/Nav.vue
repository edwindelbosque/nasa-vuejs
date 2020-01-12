<template>
  <nav>
    <div>
      <img alt="NASA logo" src="../assets/logo.png" class="logo" />
      <h2>Photo of the day</h2>
    </div>
    <Date />
  </nav>
</template>

<script>
import Date from "./Date";

export default {
  name: "Nav",
  components: {
    Date
  }
};
</script>

<style scoped>
nav {
  display: flex;
  width: 1000px;
  justify-content: space-between;
}

div {
  display: flex;
  align-items: center;
}

.logo {
  width: 120px;
  height: auto;
}

h2 {
  color: white;
}
</style>