<template>
  <h2 v-if="num === 0">The Number is Zero</h2>
  <h2 v-else-if="num < 0">The number is negative</h2>
  <h2 v-else-if="num > 0">The number is positive</h2>
  <h2 v-else>Not a number</h2>

  <div v-if="display">
    <h2>Hafizh</h2>
    <h2>WP 17</h2>
    <h2>Vue js</h2>
  </div>

  <hr />

  <div v-show="showElement">
    <h2>Hafizh</h2>
    <h2>WP 17</h2>
    <h2>Vue js</h2>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      num: "hahha",
      display: true,
      showElement: false,
    }
  },
}
</script>

<style scoped>
.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: #00ff00;
}

.sold-out {
  color: #ff0000;
}
</style>
