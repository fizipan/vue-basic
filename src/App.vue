<template>
  <div>
    <pre>
    {{ JSON.stringify(formInput, null, 2) }}
  </pre
    >
  </div>
  <form>
    <div>
      <label for="name">Name</label>
      <input id="name" v-model.trim="formInput.name" type="text" autocomplete="off" />
    </div>

    <div>
      <label for="profile">Profile</label>
      <textarea id="profile" v-model.trim="formInput.profile" autocomplete="off"></textarea>
    </div>

    <div>
      <label for="country">Country</label>
      <select name="country" id="country" v-model="formInput.country">
        <option value="">Select Country</option>
        <option>Japan</option>
        <option>United States</option>
        <option>United Kingdom</option>
      </select>
    </div>

    <div>
      <label for="jobLocation">Job Location</label>
      <select name="jobLocation" id="jobLocation" multiple v-model="formInput.jobLocation">
        <option>Japan</option>
        <option>United States</option>
        <option>United Kingdom</option>
      </select>
    </div>

    <div>
      <input type="checkbox" name="remoteWork" id="remoteWork" v-model="formInput.remoteWork" />
      <label for="remoteWork">Remote Work</label>
    </div>
  </form>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      formInput: {
        name: "",
        profile: "",
        country: "",
        jobLocation: [],
        remoteWork: false,
        skillSet: [],
      },
    }
  },
  methods: {},
}
</script>

<style scoped>
label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}

input,
textarea,
select {
  width: 100%;
  border: 1px solid #ccc;
  border-radius: 3px;
  padding: 5px;
  margin-bottom: 5px;
}

input[type="checkbox"] {
  width: auto;
  margin-right: 10px;
}

input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}
</style>
