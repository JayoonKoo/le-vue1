<template>
  <div>
    <AppHeader v-on:renew="renewStr" v-bind:header="str" />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
export default {
  data: function () {
    return {
      str: "헤더",
    };
  },
  components: {
    AppHeader,
  },
  methods: {
    renewStr: function () {
      this.str = "hi";
    },
  },
};
</script>

<style></style>
