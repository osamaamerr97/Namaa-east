<template >
    <div class="faqs" id="faqs">
        <b-container class="bv-example-row my-5 py-5">
            <h2 class="text-center font-weight-bolder mb-5 ">{{ $t("Faqs.Faqs") }}</h2>
                <b-row class="">             
                    <b-col  cols="12" md="7" class="mb-3 mb-md-5">

                        <ul class="faq-accordion text-md">
                            <li v-for="index in 5" :key="index">
                                <input class="faq-input" type="radio" name="faq" :id="`faq-${index}`" />
                                <label class="faq-label" :for="`faq-${index}`">{{ $t(`Faqs.Question${index}`) }}<font-awesome-icon icon="fa-solid fa-chevron-down" class="icon"/></label>
                                <div class="faq-content">
                                    <p>
                                        {{ $t(`Faqs.Answer${index}`) }} <br />
                                    </p>
                                </div>
                            </li>
                        </ul>
                    </b-col>
                    <b-col cols="12" md="5" class="mb-3 mb-md-5" >
                        <div class="faqs-img  d-flex align-items-center h-100">
                            <img src="~/assets/images/kaitlyn-baker-vZJdYl5JVXY-unsplash@2x.png" class="w-100 h-100" alt="">
                        </div>
                    </b-col>
                </b-row>
            </b-container>
    </div>
</template>
<script>
export default {
    name:"Faqs" ,
    computed:{
        
    }   
}
</script>
<style scoped>
@media screen and (min-width:1199px){
    [dir="rtl"] .section-faq{
        padding-right: 60px!important;
        padding-left: 18px!important;
        padding-top: 50px!important;
    }
    [dir="ltr"] .section-faq{
        padding-left: 60px!important;
        padding-right: 18px!important;
        padding-top: 50px!important;
    }
}
@media screen and (max-width:992px){
     .section-faq h2{
        margin-top: 2.7rem;
        margin-bottom: 2rem !important;
    }
  
}
</style>