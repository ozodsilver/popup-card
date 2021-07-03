<template>
  <div id="app">
    <card> </card>
  </div>
</template>

<script>
import card from "./components/card.vue";
export default {
  el: "#app",
  components: {
    card,
  },

  data() {
    return {};
  },

  methods: {},
};
</script>

<style>
body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background: rgb(177, 187, 206);
}
</style>
