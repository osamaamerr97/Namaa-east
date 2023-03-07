<template>
    <div :dir="getPageDirection">
      <TheHeader :class="{change_color: scrollPosition > 50}"/>
        <nuxt-child />
      <TheFooter />
    </div>
  </template>
  <script>
  export default {
    name: 'IndexPage',
    data() {
      return {
        scrollPosition: null

      }
    },
  computed:{
    getPageDirection() {
      if (this.$i18n.locale == "ar") {
        return "rtl";
      }
      return "ltr";
    },
  },
  methods: {
    updateScroll() {
      console.log( window.scrollY);
       this.scrollPosition = window.scrollY
    }
},
  mounted() {
    if(window.scrollY !=0){
      this.updateScroll()
    }
    window.addEventListener('scroll', this.updateScroll);
  }
  }
  </script>
  <style scoped>
  .change_color {
      background-color:#6C1835 !important;
      padding-bottom: 20px;
  }
</style>
  