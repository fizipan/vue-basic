<template>
  <h2>Volume Tracker (0-20)</h2>
  <h2>Current Volume {{ volume }}</h2>
  <div>
    <button @click="volume += 2">Increase</button>
    <button @click="volume -= 2">Decrease</button>
  </div>
  <input type="text" v-model="movie" />
  <input type="text" v-model="movieInfo.title" />
  <input type="text" v-model="movieInfo.actor" />
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      volume: 0,
      movie: "hafizh",
      movieInfo: {
        title: "",
        actor: "",
      },
    }
  },
  watch: {
    volume(newVolume, oldValue) {
      if (newVolume > oldValue && newVolume === 16) {
        alert("Volume at max!")
      }
    },
    movie: {
      handler(newValue) {
        console.log("calling api =", newValue)
      },
      immediate: true,
    },
    movieInfo: {
      handler(newValue) {
        console.log("calling api =", newValue)
      },
      deep: true,
    },
  },
}
</script>

<style scoped></style>
