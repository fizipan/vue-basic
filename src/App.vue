<template>
  <div>{{ greet }} {{ name }}</div>
  <div v-text="channel"></div>
  <div v-html="channelHtml"></div>
  <div v-html="hack"></div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      greet: "Hello",
      name: "Hafizh Maulana",
      channel: "Web Programming 17",
      channelHtml: "<b>Web Programming 17</b>",
      hack: `<a href="#" onclick="alert('You have been hacked')">Win a Prize</a>`,
    }
  },
}
</script>

<style scoped></style>
