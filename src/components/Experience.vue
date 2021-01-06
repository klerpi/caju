<template lang="pug">
.resume-section
  h2(v-if="lang === 'br'") Experiência
  h2(v-else) Experience

  .experience-items
    .item(v-for="(experience, index) in experiences", key="exp-{{index}}")
      h3 {{ experience.title }}
      h4.accent-color {{ experience.company }}
      span.icon-with-text
        i.material-icons.accent-color calendar_today
        span {{ experience.timeSpan }}
      ul.experience-highlights
        li(
          v-for="(highlight, index) in experience.highlights",
          key="high-{{index}}"
        ) {{ highlight }}
</template>

<script>
export default {
  props: ["lang", "experiences"],
};
</script>

<style lang="scss" scoped>
i {
  font-size: 16px;
}

.experience-highlights {
  margin-top: 6px;
}
</style>