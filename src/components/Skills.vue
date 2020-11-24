<template lang="pug">
.resume-section
  h2(v-if="lang === 'br'") Habilidades
  h2(v-else) Skills
</template>

<script>
export default {
  props: ["lang", "skills"],
};
</script>

<style lang="scss" scoped>
</style>