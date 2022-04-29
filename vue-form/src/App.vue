<template>
  <form v-on:submit.prevent="onSubmit">
    <label>
      id:
      <input type="text" v-model="username" />
    </label>
    <label>
      password:
      <input type="password" v-model="password" />
    </label>
    <button type="submit">로그인</button>
  </form>
</template>

<script>
import axios from "axios";
const url = "https://jsonplaceholder.typicode.com/users";
export default {
  data: () => {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    onSubmit: async function () {
      const { data } = await axios.post(url, {
        username: this.username,
        password: this.password,
      });
      console.log(data);
    },
  },
};
</script>

<style></style>
