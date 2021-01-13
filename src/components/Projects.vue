<template lang="pug">
.resume-section
  h2(v-if="lang === 'br'") Projetos Pessoais
  h2(v-else) Personal Projects

  .project-items
    .item(v-for="(project, index) in projects", key="exp-{{index}}")
      h3 {{ project.title }}
      h4.accent-color {{ project.technologies }}
      ul.project-highlights
        li(
          v-for="(highlight, index) in project.highlights",
          key="high-{{index}}"
        ) {{ highlight }}
</template>

<script>
export default {
  props: ["lang", "projects"],
};
</script>

<style lang="scss" scoped>
i {
  font-size: 16px;
}

.project-highlights {
  margin-top: 6px;
}
</style>