<template>
  <h2>List Names</h2>
  <ul>
    <li v-for="(name, index) in names" :key="index">{{ index + 1 }}. {{ name }}</li>
  </ul>
  <hr />
  <h2>List Fullnames</h2>
  <ul>
    <li v-for="fullname in fullNames" :key="fullname.firstName">
      {{ fullname.firstName }} {{ fullname.lastName }}
    </li>
  </ul>
  <hr />
  <h2>List Actors</h2>
  <ul>
    <li v-for="actor in actors" :key="actor.name">
      {{ actor.name }}
      <ul>
        <li v-for="movie in actor.movies" :key="movie">
          {{ movie }}
        </li>
      </ul>
    </li>
  </ul>
  <h2>List Actors</h2>
  <ul>
    <li v-for="(info, key, index) in myInfo" :key="info.name">
      {{ index + 1 }}. {{ key }}: {{ info }}
    </li>
  </ul>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      names: ["John", "Jane", "Joe"],
      fullNames: [
        {
          firstName: "Bruce",
          lastName: "Wayne",
        },
        {
          firstName: "Clark",
          lastName: "Kent",
        },
        {
          firstName: "Midun",
          lastName: "Doe",
        },
      ],
      actors: [
        {
          name: "Hafizh",
          movies: ["The Avengers", "The Dark Knight", "The Dark Knight Rises"],
        },
        {
          name: "Haikal",
          movies: ["Spiderman", "Catwowan"],
        },
        {
          name: "Midun",
          movies: ["Pinokio", "Barudak Teuing"],
        },
      ],
      myInfo: {
        name: "Hafizh",
        age: 20,
        address: "Jl. Raya",
      },
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
