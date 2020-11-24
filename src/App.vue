<template lang="pug">
#app
  h1 Hello, {{ myData.name }}.
</template>

<script>
// Import your data here (remove the "example")
import json from "../data/data.example.json";

export default {
  name: "App",
  components: {},
  data() {
    return {
      myData: json,
    };
  },
};
</script>

<style lang="scss">
@import "~minireset.css/minireset.css";
@import "~paper-css/paper.min.css";
</style>
