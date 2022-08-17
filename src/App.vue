<template>
  <h2>{{ name }}</h2>
  <div>
    <button @click="changeName($event), increment(2, $event)">Chnage Name</button>
  </div>
  <hr />
  <h2>Count: {{ count }}</h2>
  <div>
    <button @click="increment(2, $event)">Increment 2</button>
    <button @click="decrement(2, $event)">Decrement 2</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      name: "Vue",
      count: 0,
    }
  },
  methods: {
    changeName(e) {
      this.name = "Hafizh"
      console.log(e)
    },
    increment(num, event) {
      this.count += num
      console.log(event)
    },
    decrement(num, event) {
      if (this.count > 0) {
        this.count -= num
        console.log(event)
      } else {
        alert("Count cannot be less than 0")
      }
    },
  },
}
</script>

<style scoped></style>
