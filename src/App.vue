<template>
  <template v-for="name in names" :key="name">
    <h2>
      {{ name }}
    </h2>
    <input type="text" placeholder="Las Name" />
    <hr />
  </template>
  <button @click="shuffle">Shuffle</button>
</template>

<script>
import _ from "lodash"
export default {
  name: "App",
  data() {
    return {
      names: ["John", "Jane", "Joe"],
    }
  },
  methods: {
    shuffle() {
      this.names = _.shuffle(this.names)
    },
  },
}
</script>

<style scoped></style>
