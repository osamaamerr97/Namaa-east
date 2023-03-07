<template>
<div>
  <HomeHeader></HomeHeader>
    <ourServices></ourServices>
    <faq></faq>
    <OurBlogs></OurBlogs>
</div>


</template>
<script>

import ourServices from '@/components/Home/OurServices.vue'
import faq from '@/components/Home/Faqs.vue'
import OurBlogs from '../components/Home/OurBlogs.vue'
import HomeHeader from '../components/Home/HomeHeader.vue'
export default {
  name: 'IndexPage',
  components:{
    ourServices,
    faq,
    OurBlogs,
    HomeHeader

  }
}  
</script>
