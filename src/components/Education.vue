<template lang="pug">
.resume-section
  h2(v-if="lang === 'br'") Formação
  h2(v-else) Education

  .education-items
    .item(v-for="(edItem, index) in education", key="ed-{{index}}")
      h3 {{ edItem.title }}
      h4.accent-color {{ edItem.institution }}
      span.icon-with-text
        i.material-icons.accent-color calendar_today
        span {{ edItem.timeSpan }}
</template>

<script>
export default {
  props: ["education", "lang"],
};
</script>

<style lang="scss" scoped>
i {
  font-size: 16px;
}
</style>