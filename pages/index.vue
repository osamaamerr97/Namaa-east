<template>

<div id="home-head" class="home-header">
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
</template>
<script>
export default {
  name: 'IndexPage',
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
