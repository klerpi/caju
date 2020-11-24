<template lang="pug">
#app
  Header(
    :name="myData.name",
    :desiredPosition="myData.desiredPosition",
    :contactInfo="myData.contactInfo"
  )
  Skills(:skills="myData.skills", :lang="lang")
</template>

<script>
// Import your data here (remove the "example")
import json from "../data/data.example.json";

import Header from "./components/Header";
import Skills from "./components/Skills";

export default {
  name: "App",
  components: {
    Header,
    Skills,
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

@page {
  size: A4;
}

body {
  font-family: "Mulish", sans-serif;
  font-size: 16px;
}

i {
  margin-right: 10px;
}

.icon-with-text {
  display: inline-flex;
  font-size: 14px;
  align-items: center;
  margin-right: 14px;
  font-weight: 500;
}

.accent-color {
  color: #5f1609;
}
</style>
