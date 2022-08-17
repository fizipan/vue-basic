<template>
  <template v-for="name in names" :key="name">
    <h2 v-if="name === 'John'">
      {{ name }}
    </h2>
  </template>
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
