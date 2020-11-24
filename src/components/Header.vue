<template lang="pug">
section.header
  h1 Hello, {{ name }}.
</template>

<script>
export default {
  props: ["name", "desiredPosition", "contactInfo"],
};
</script>

<style lang="scss">
</style>