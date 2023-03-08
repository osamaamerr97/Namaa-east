<template>
<div>
  <HomeHeader></HomeHeader>
    <ourServices></ourServices>
    <OurSolutions></OurSolutions>
  <OurPartners></OurPartners>
    <faq></faq>
    <OurBlogs></OurBlogs>
    <Contact></Contact>
</div>


</template>
<script>

import ourServices from '@/components/Home/OurServices.vue'
import faq from '@/components/Home/Faqs.vue'
import OurBlogs from '../components/Home/OurBlogs.vue'
import HomeHeader from '../components/Home/HomeHeader.vue'
import OurSolutions from '../components/Home/OurSolutions.vue'
import OurPartners from '../components/Home/OurPartners.vue'
import Contact from '../components/Home/contact.vue'
export default {
  name: 'IndexPage',
  components:{
    ourServices,
    faq,
    OurBlogs,
    HomeHeader,
    OurSolutions,
    OurPartners,
    Contact

  }
}  
</script>
