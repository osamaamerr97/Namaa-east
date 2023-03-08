<template>
    <div class="our-partners">
        <b-container class="mt-5 pt-5">
                <b-row class="">
                    <b-col class="" cols="12" md="6" >
                        <div  class="d-flex align-items-center h-100">
                            <div class="">
                                <h2>{{$t('ourPartners.our')}}  <span> {{$t('ourPartners.Partners')}}</span></h2>
                                <p class="des1">{{$t('ourPartners.des1')}}</p>
                                <p class="des2">{{$t('ourPartners.des2')}}</p>
                            </div>
                        </div>
                    </b-col>
                    <b-col class="" v-for="partner in partners" cols="12" md="6">
                        <div class="img-contanier">
                                <img  :src="partner" alt="ICON">
                        </div>
                    </b-col>
                </b-row>
            </b-container>
    </div>
</template>
<script>
export default {
    name:"our-partners",
    data() {
        return {
            partners:[
                'Component 41 – 3.png',
                'Component 43 – 3.png',
                'Component 42 – 3.png'            
            ]
        }
    },
    
}
</script>
<style lang="">
    
</style>