<template lang="">
    <div class="nav-container bg-main">
      <div class="container">
        <nav>
            <div class="logo">
                <img src="~/assets/images/logo.svg" style="width:140px" alt="" srcset="">
            </div>
            <div class="hamburger "  @click="toggleMenu" :class="{'toggle': isMenuOpen ==true}">
                <div class="line1"></div>
                <div class="line2"></div>
                <div class="line3"></div>
            </div>
            <ul class="nav-links" :class="{'open': isMenuOpen ==true}">
              <li class="nav-link"  :class="{'fade': isMenuOpen ==true}">
                <nuxtLink :to="localePath('/')" class='active'>{{ $t('navbar.Home')}}</nuxtLink>
              </li>
              <li class="nav-link" :class="{'fade': isMenuOpen ==true}">
                <nuxtLink :to="localePath('/')" >{{ $t('navbar.Company')}}</nuxtLink>
              </li>              
              <li class="nav-link" :class="{'fade': isMenuOpen ==true}">
                <nuxtLink :to="localePath('/')" >{{ $t('navbar.Services')}}</nuxtLink>
              </li>
              <li class="nav-link" :class="{'fade': isMenuOpen ==true}">
                <nuxtLink :to="localePath('/')" >{{ $t('navbar.Solutions')}}</nuxtLink>
              </li>
              <li class="nav-link" :class="{'fade': isMenuOpen ==true}">
                <nuxtLink :to="localePath('/')" >{{ $t('navbar.Our_Work')}}</nuxtLink>
              </li>
              <li class="nav-link" :class="{'fade': isMenuOpen ==true}">
                <nuxtLink :to="localePath('/')" >{{ $t('navbar.Blog')}}</nuxtLink>
              </li>
              <li  class=' lang' :class="{'fade': isMenuOpen ==true}">
                <div class="nav-wrapper ">
                    <div class="sl-nav">
                        <ul>
                        <li><img src="~/assets/images/lang.svg" alt="" srcset=""> {{this.$i18n.locale =="en"?"English":"العربية"}} <font-awesome-icon icon="fa-solid fa-angle-down" /></i>
                            <div class="triangle"></div>
                            <ul>
                                <li  v-for="lang in languages" :key="lang.value" :value="lang.value" @click="changeLang(lang.value)">
                                     <nuxt-link to=""> 
                                         <span  v-if="selectedLang == 'en'" class="flag"><i v-if="lang.value =='en'" class="sl-flag flag-usa" ><div id="flag-ar"></div></i>  <i v-else class="sl-flag flag-ar" ><div id="flag-ar"></div></i></span>    
                                         <span :class="[selectedLang == lang.value?'active':'']">{{ lang.text }}</span>
                                        <span v-if="selectedLang == 'ar'" class="flag"><i v-if="lang.value =='en'" class="sl-flag flag-usa" ><div id="flag-ar"></div></i>  <i v-else class="sl-flag flag-ar" ><div id="flag-ar"></div></i></span>    
                                    </nuxt-link>                                     
                                </li>
                            </ul>
                        </li>
                        </ul>
                    </div>
                </div>
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
      selectedLang: this.$i18n.locale,
      languages: [
        { text: "English", value: "en", icon: "gb" },
        { text: "العربية", value: "ar", icon: "sa" },
      ],
    }
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    changeLang(lang) {
      if (lang == "en") {
        this.$i18n.setLocale(lang);
        this.selectedLang= 'en'
      } else {
        this.$i18n.setLocale("ar");
        this.selectedLang= 'ar'
      }
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
    justify-content: space-between;
    list-style: none; 
    margin-left: auto;
    width: 65%;
    margin-bottom: 0;
}
.nav-links:dir(rtl){ /* ul */
    margin-left: unset;
    margin-right: auto;   
}
.nav-links li {
    position: relative;
    padding-bottom: 15px;
    text-align: center;
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
.nav-link:hover::before,
.nav-link .active::before{
    content: '';
    height: 2px;
    background-color: #c38ea0;
    position: absolute;
    bottom: 0;
    transition:width 3s;
    z-index: 999;
    width: 90%;
    left:  5px;
}
.nav-link::before:dir(rtl),
.nav-link:hover::before:dir(rtl),
.nav-link .active::before:dir(rtl){
    left:  unset;
    right:  5px;
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
.lang{
    display: flex;
    align-items: center;
    padding-bottom: 0 !important;    
}
.nav-wrapper {
  text-align: center;
}
.sl-nav {
  display: inline;
}
.sl-nav ul {
  margin:0;
  padding:0;
  list-style: none;
  position: relative;
  display: inline-block;
}
.sl-nav li {
  cursor: pointer;
  padding-bottom:10px;
}
.sl-nav li ul {
  display: none;
}
.sl-nav li:hover ul {
  position: absolute;
  top:29px;
  right:-15px;
  display: block;
  background: #fff;
  width: 120px;
  padding-top: 0px;
  z-index: 1;
  border-radius:5px;
  box-shadow: 0px 0px 20px rgba(0,0,0,0.2);
}
.sl-nav li:hover ul:dir(rtl){
    right:unset;
    left:-15px;
}
.sl-nav li:hover .triangle {
  position: absolute;
  top: 15px;
  right: -10px;
  z-index:10;
  height: 14px;
  overflow:hidden;
  width: 30px;
  background: transparent;
}
.sl-nav li:hover .triangle:dir(rtl){
    right: unset;
    left: -10px;
}
.sl-nav li:hover .triangle:after {
  content: '';
  display: block;
  z-index: 20;
  width: 15px;
  transform: rotate(45deg) translateY(0px) translatex(10px);
  height: 15px;
  background: #fff;
  border-radius:2px 0px 0px 0px;
  box-shadow: 0px 0px 20px rgba(0,0,0,0.2);
}
.sl-nav li:hover .triangle:after:dir(rtl){
    border-radius:0px 0px 0px 0px;
    transform: rotate(-45deg) translateY(0px) translatex(-10px);
}
.sl-nav li ul li {
  position: relative;
  text-align: left;
  background: transparent;
  padding: 15px 15px;
  padding-bottom:0;
  z-index: 2;
  font-size: 15px;
  color: #3c3c3c;
}
.sl-nav li ul li:last-of-type {
  padding-bottom: 15px;
}
.sl-nav li ul li span  {
  color: black;
}
.sl-nav li ul li span:hover, .sl-nav li ul li span.active {
  color: #c38ea0;
}
.sl-flag {
  display: inline-block;
  box-shadow: 0px 0px 3px rgba(0,0,0,0.4);
  width: 15px;
  height: 15px;
  background: #aaa;
  border-radius: 50%;
  position: relative;
  top: 2px;
  overflow: hidden;
}
.flag-ar {
    background: url('~/assets/images/saudi-arabia.svg');
  background-size: cover;
  background-position: center center;
}
.flag-usa {
  background-size: cover;
  background-position: center center;
  background: url('~/assets/images/united-kingdom.svg');
}

/*Stying for small screens*/
@media screen and (max-width: 992px){
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
    .hamburger:dir(rtl){ 
        right:unset; 
        left: 5%; 
    }
    .nav-links{
        position: fixed;
        left: 0;
        bottom: 0;
        justify-content: start;
        background: #040303;
        opacity: 0.7;
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
    .nav-links:dir(rtl){
        clip-path: circle(50px at 20% -20%);
        -webkit-clip-path: circle(50px at 20% -10%);
    }
    .nav-links.open{
        clip-path: circle(850px at 100% -10%);
        -webkit-clip-path: circle(850px at 100% -10%);
        pointer-events: all;
    }
    .nav-links.open:dir(rtl){
        clip-path: circle(850px at 0% -10%);
        -webkit-clip-path: circle(850px at 0% -10%);
    }
    .nav-links > li{
        opacity: 0;
        margin-top: 20px;
        display: inline-block;
    }
    .nav-links > li:first-child{
        margin-top: 100px;
    }
    .nav-links > li:last-child{
        margin-top: 20px !important; 
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
    }
    .nav-links li:nth-child(7){
        transition: all 0.5s ease 1s;
        margin: 0;
    }
    li.fade{
        opacity: 1;
    }
    .nav-link::before{
        right: unset;
        left: 40%;
    }
    .nav-link:hover::before,
    .nav-link .active::before{
        right: unset;
        width: 20%;
        left:  40%;
    }
    .nav-link::before:dir(rtl){
        left: unset;
        right: 40%;
    }
    .nav-link:hover::before:dir(rtl),
    .nav-link .active::before:dir(rtl){
        width: 20%;
        left:  unset;
        right:  40%;
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