<template lang="">
    <div class="nav-container bg-main">
      <div class="container">
        <nav>
            <div class="logo">
                <!-- <img src="logo.svg" alt="Logo Image"> -->
                <h2>Namaa</h2>
            </div>
            <div class="hamburger "  @click="toggleMenu" :class="{'toggle': isMenuOpen ==true}">
                <div class="line1"></div>
                <div class="line2"></div>
                <div class="line3"></div>
            </div>
            <ul class="nav-links" :class="{'open': isMenuOpen ==true}">
              <li class="nav-link"  :class="{'fade': isMenuOpen ==true}">
                <nuxtLink to="#" class='active'>Home</nuxtLink>

              </li>
              <li class="nav-link" :class="{'fade': isMenuOpen ==true}">
                <nuxtLink to="#">Solutions</nuxtLink>

              </li>
              
              <li class="nav-link" :class="{'fade': isMenuOpen ==true}">
                <nuxtLink to="#">Industries</nuxtLink>

              </li>
              <li class="nav-link" :class="{'fade': isMenuOpen ==true}">
                <nuxtLink to="#">Portfolio</nuxtLink>

              </li>
              <li class="nav-link" :class="{'fade': isMenuOpen ==true}">
                <nuxtLink to="#">About Us</nuxtLink>

              </li>
            </ul>
        </nav>
      </div>
    </div>
</template>



<script>
export default {
  data() {
    return {
      isMenuOpen: false,
    }
  },
  methods: {
    toggleMenu() {

      //Hamburger Animation
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
    
}
</script>
<style scoped>
.nav-container{
  position: fixed;

  top: 0;
    left: 0;
    right: 0;
    z-index: 99;
}
nav{
    padding-top: 30px;
    padding-bottom: 1px;
    width: 100%;
    display: flex;
    align-items: center;
    color: #FFF;

}

/*Styling Links*/
.nav-links{   /* ul */
    display: flex;
    justify-content: space-around;
    list-style: none; 
    align-items: center;
    margin-left: auto;
    width: 50%;
    margin-bottom: 0;

}
.nav-links li {
    position: relative;
    padding-bottom: 15px;
}
.nav-links li a{
    text-decoration: none;
    color: #DDD;
}


.nav-link::before{
    content: '';
    width: 0%;
    height: 2px;
    background-color: #c38ea0;
    position: absolute;
    left:  5px;
    bottom: 0;
    transition:width 3s;
    z-index: 999;

}
.nav-links li:hover a,
.nav-link .active {
    color: #FFF !important;
}
.nav-link:hover::before{
    content: '';
    width: 90%;
    height: 2px;
    background-color: #c38ea0;
    position: absolute;
    left:  5px;
    bottom: 0;
}


.nav-link .active::before{
    content: '';
    width: 90%;
    height: 2px;
    background-color: #c38ea0;
    position: absolute;
    left:  5px;
    bottom: 0;
}



/*Styling Hamburger Icon*/
.hamburger div{
    width: 30px;
    height:3px;
    background: #f2f5f7;
    margin: 5px;
    transition: all 0.3s ease;
}
.hamburger{
    display: none;
}

/*Stying for small screens*/
@media screen and (max-width: 800px){
    nav{
        position: relative;
        z-index: 999;
    }
    .hamburger{
        display:block;
        position: absolute;
        cursor: pointer;
        right: 5%;
        top: 50%;
        transform: translate(-5%, -50%);
        z-index: 2;
        transition: all 0.7s ease;
    }
    .nav-links{
        position: fixed;
        left: 0;
        bottom: 0;
        justify-content: start;

        background: #666565;
        /* opacity:.5; */
        height: 100vh;
        width: 100%;
        flex-direction: column;
        clip-path: circle(50px at 90% -20%);
        -webkit-clip-path: circle(50px at 90% -10%);
        transition: all 1s ease-out;
        pointer-events: none;
        padding: 0;
        margin: 0;
    }
    .nav-links.open{
        clip-path: circle(1000px at 90% -10%);
        -webkit-clip-path: circle(1000px at 90% -10%);
        pointer-events: all;
    }
    .nav-links li{
        opacity: 0;
        margin-top: 60px;
    }
    .nav-links li:nth-child(1){
        transition: all 0.5s ease 0.2s;
    }
    .nav-links li:nth-child(2){
        transition: all 0.5s ease 0.4s;
    }
    .nav-links li:nth-child(3){
        transition: all 0.5s ease 0.6s;
    }
    .nav-links li:nth-child(4){
        transition: all 0.5s ease 0.7s;
    }
    .nav-links li:nth-child(5){
        transition: all 0.5s ease 0.8s;
    }
    .nav-links li:nth-child(6){
        transition: all 0.5s ease 0.9s;
        margin: 0;
    }
    .nav-links li:nth-child(7){
        transition: all 0.5s ease 1s;
        margin: 0;
    }
    li.fade{
        opacity: 1;
    }
}
/*Animating Hamburger Icon on Click*/
.toggle .line1{
    transform: rotate(-45deg) translate(-5px,6px);
}
.toggle .line2{
    transition: all 0.7s ease;
    width:0;
}
.toggle .line3{
    transform: rotate(45deg) translate(-5px,-6px);
}
</style>