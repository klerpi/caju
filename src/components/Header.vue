<template lang="pug">
.resume-section
  h1 {{ name }}
  p.accent-color {{ desiredPosition }}
  .contact-info
    span.icon-with-text
      i.material-icons.accent-color email
      span {{ contactInfo.email }}
    span.icon-with-text
      i.material-icons.accent-color phone
      span {{ contactInfo.phone }}
    span.icon-with-text
      i.material-icons.accent-color link
      span {{ contactInfo.website }}
</template>

<script>
export default {
  props: ["name", "desiredPosition", "contactInfo"],
};
</script>

<style lang="scss" scoped>
h1 {
  font-size: 42px;
  font-weight: 800;
}

i {
  font-size: 20px;
}

p {
  font-weight: bold;
  font-size: 22px;
  margin-bottom: 8px;
}
</style>