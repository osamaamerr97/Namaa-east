<template>
    <div :dir="getPageDirection">
      <TheHeader />
        <nuxt-child />
      <TheFooter />
    </div>
  </template>
  <script>
  export default {
    name: 'IndexPage',
  computed:{
    getPageDirection() {
      if (this.$i18n.locale == "ar") {
        return "rtl";
      }
      return "ltr";
    },
  }
  }
  </script>
  