<template>
  <section>
    <h2>NEBULA GALAXY</h2>
    <div>
      <img
        alt="Photo of the day by NASA."
        src="https://apod.nasa.gov/apod/image/1912/M33-HaLRGB-RayLiao.jpg"
      />
    </div>
  </section>
</template>

<script>
export default {
  name: "PhotoHolder"
};
</script>

<style scoped>
section {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: flex-start;
}

h2 {
  color: #d5dadd;
  background: #1a212c;
  padding: 0px 10px;
  padding-top: 3px;
  font-weight: 800;
  letter-spacing: 1px;
  text-align: left;
}

div {
  margin-top: 12px;
  width: 1000px;
  height: fit-content;
  display: flex;
  justify-content: center;
  align-content: flex-start;
  padding-bottom: 1px;
  background: #334055;
}

img {
  width: 998px;
  height: auto;
  margin-top: 1px;
}
</style>