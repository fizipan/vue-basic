<template>
  <div>{{ greet }} {{ name }}</div>
  <div v-text="channel"></div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      greet: "Hello",
      name: "Hafizh Maulana",
      channel: "Web Programming 17",
    }
  },
}
</script>

<style scoped></style>
