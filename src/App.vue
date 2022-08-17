<template>
  <h2>{{ 2 + 3 + 5 }}</h2>
  <h2>{{ 5 + 10 + 15 }}</h2>
  <h2>Add Method - {{ add(2, 3, 10) }}</h2>
  <h2>Add multiply - {{ multiply(20) }}</h2>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      baseMultiplier: 2,
    }
  },
  methods: {
    add(a, b, c) {
      return a + b + c
    },
    multiply(num) {
      return num * this.baseMultiplier
    },
  },
}
</script>

<style scoped></style>
