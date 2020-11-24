<template lang="pug">
section.header
  h1 {{ name }}
  p {{ desiredPosition }}
  .contact-info
    span.icon-with-text
      i.material-icons email
      span {{ contactInfo.email }}
    span.icon-with-text
      i.material-icons sms
      span {{ contactInfo.phone }}
    span.icon-with-text
      i.material-icons link
      span {{ contactInfo.website }}
</template>

<script>
export default {
  props: ["name", "desiredPosition", "contactInfo"],
};
</script>

<style lang="scss">
</style>