<template lang="pug">
#app
  Header(
    :name="myData.name",
    :desiredPosition="myData.desiredPosition",
    :contactInfo="myData.contactInfo"
  )
  Skills(:skills="myData.skills", :lang="lang")
  Experience
</template>

<script>
// Import your data here (remove the "example")
import json from "../data/data.example.json";

import Header from "./components/Header";
import Skills from "./components/Skills";
import Experience from "./components/Experience";

export default {
  name: "App",
  components: {
    Header,
    Skills,
    Experience,
  },
  data() {
    return {
      lang: "en",
      myData: json,
    };
  },
};
</script>

<style lang="scss">
@import "~minireset.css/minireset.css";
@import "~paper-css/paper.min.css";
@import "main.scss";
</style>
