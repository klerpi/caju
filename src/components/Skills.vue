<template lang="pug">
section.skills
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