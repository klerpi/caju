<template lang="pug">
.resume-section
  h2(v-if="lang === 'br'") Habilidades
  h2(v-else) Skills

  .skill-items
    .skill-item
      i.material-icons.accent-color settings
      .skill-item-info
        h3(v-if="lang === 'br'") Linguagens de Programação
        h3(v-else) Programming Languages
        p {{ skills.programmingLanguages }}

    .skill-item
      i.material-icons.accent-color code
      .skill-item-info
        h3(v-if="lang === 'br'") Desenvolvimento Web
        h3(v-else) Web Development
        p {{ skills.webDevelopment }}

    .skill-item
      i.material-icons.accent-color construction
      .skill-item-info
        h3(v-if="lang === 'br'") Ferramentas
        h3(v-else) Tools
        p {{ skills.tools }}

    .skill-item
      i.material-icons.accent-color language
      .skill-item-info
        h3(v-if="lang === 'br'") Línguas
        h3(v-else) Languages
        p {{ skills.languages }}
</template>

<script>
export default {
  props: ["lang", "skills"],
};
</script>

<style lang="scss" scoped>
</style>