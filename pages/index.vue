<template>
<div>
<div id="home-head" class="home-header">


  <div class="head-content">
    <div class="container">
      <h1>Empowering <br> Businesses <br> With Innovative <br> IT Solutions</h1>
      <p>Founded in the heart of Saudi Arabia, Namaa Alsharq is <br> committed to providing cutting-edge software solutions  that<br> enable businesses in the Kingdom to reach their full potential.</p>
      <button>Show More</button>
    </div>
  </div>
    <!-- <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators 
      background="#6C1835"
      img-width="1024"
      img-height="100"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide class="h-100 ">
        <div>
          <h1>Namaa <br/> Leading Mobile App <br/> Development Company</h1>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde tenetur maiores quam corporis</p>
          <button>Vieew portofolio</button>

        </div>
        
      </b-carousel-slide>
      <b-carousel-slide class="h-100 ">
        <div>
          <h1>yhgtfrhgf <br/> Leading Mobile App <br/> Development Company</h1>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde tenetur maiores quam corporis</p>
          <button>Vieew portofolio</button>

        </div>
        
      </b-carousel-slide>

    </b-carousel> -->
  </div>
    <ourServices></ourServices>
    <faq></faq>
</div>


</template>
<script>
import ourServices from '@/components/Home/OurServices.vue'
import faq from '@/components/Home/Faqs.vue'
export default {
  name: 'IndexPage',
  components:{
    ourServices,
    faq
  },
  data() {
      return {
        slide: 0,
        sliding: null
      }
    },
    methods: {
      onSlideStart(slide) {
        this.sliding = true
      },
      onSlideEnd(slide) {
        this.sliding = false
      }
    }
}
</script>
