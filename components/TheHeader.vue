<template lang="">
    <div>
      <div class="bg-main pt-2">
    <b-navbar toggleable="lg" class='container'>
      <b-navbar-brand href="#" >NavBar</b-navbar-brand>

      
      <b-navbar-toggle target="nav-collapse" toggleable @click='isNavOpen = !isNavOpen'>
        <font-awesome-icon  v-if='isNavOpen == true'  :icon="['fas', 'xmark']"  class='close-icon'/>
      </b-navbar-toggle>



      <b-collapse id="nav-collapse" is-nav>
          
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-navbar-nav>
            <b-nav-item href="#" class='active'>Home</b-nav-item>
            <b-nav-item href="#">Solutions</b-nav-item>
            <b-nav-item href="#">Industries</b-nav-item>
            <b-nav-item href="#">Portfolio</b-nav-item>
            <b-nav-item href="#">About Us</b-nav-item>
          </b-navbar-nav>

          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

        </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
    </div>
</template>
<script>
export default {
  data() {
    return {
      isNavOpen:false
    }
  },
    
}
</script>
<style lang="">
    
</style>