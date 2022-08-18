<template>
  <h2>Fullname - {{ firstName }} {{ lastName }}</h2>
  <button @click="changeName">Change Name</button>
  <h2>Computed Fullname - {{ fullName }}</h2>
  <h2>Total - {{ items.reduce((total, item) => total + item.price, 0) }}</h2>
  <h2>Computed Total - {{ total }}</h2>
  <button @click="items.push({ id: 4, name: 'New Item', price: 10 })">Add Item</button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      firstName: "Hafizh",
      lastName: "Maulana",
      items: [
        { id: 1, title: "TV", price: 100 },
        { id: 2, title: "Laptop", price: 200 },
        { id: 3, title: "Kulkas", price: 50 },
      ],
    }
  },
  methods: {
    changeName() {
      this.fullName = "Syatya Athary"
    },
  },
  computed: {
    fullName: {
      get() {
        return this.firstName + " " + this.lastName
      },
      set(newValue) {
        const names = newValue.split(" ")
        this.firstName = names[0]
        this.lastName = names[1]
      },
    },
    total() {
      return this.items.reduce((total, item) => total + item.price, 0)
    },
  },
}
</script>

<style scoped></style>
