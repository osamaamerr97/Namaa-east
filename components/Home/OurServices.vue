<template>
    <div>
        <div class="our-services">
            <b-container class="bv-example-row mt-5 pt-5">
                <b-row class="">
                    <b-col class="colum" cols="12" md="6" lg="4" >
                    <div class="d-flex align-items-center h-100">
                        <h2><span>{{$t('OurServices.Our')}}  </span> <br> {{$t('OurServices.Services')}}</h2>
                    </div>
                    </b-col>
                    <b-col class="colum" v-for="service in services" :key="service.titlePart1" cols="12" md="6" lg="4" >
                        <div class="service">
                            <div class="service-title d-flex align-items-center justify-content-between">
                                <h4>  {{$t(service.titlePart1)}}  <br> {{$t(service.titlePart2)}} </h4>
                                <img  v-bind:src="'/_nuxt/assets/images/' + service.icon +'.png'" alt="ICON">
                            </div>
                            <div class="service-description"> {{ $t(service.description)}}</div>
                        </div>
                    </b-col>
                </b-row>
            </b-container>
        </div>
    </div>
</template>
<script>
export default {
    name:"our-services",
    data() {
        return {
            services:[
                {
                    titlePart1:"OurServices.Application",
                    titlePart2:"OurServices.Development",
                    icon:"coding",
                    description:"OurServices.des"
                },
                {
                    titlePart1:"OurServices.Consulting",
                    titlePart2:"OurServices.Advisory",
                    icon:"tv",
                    description:"OurServices.des"
                },
                {
                    titlePart1:"OurServices.Design",
                    titlePart2:"OurServices.Production",
                    icon:"color-palette",
                    description:"OurServices.des"
                },
                {
                    titlePart1:"OurServices.Sales",
                    titlePart2:"OurServices.Marketing",
                    icon:"megaphone",
                    description:"OurServices.des"
                },
                {
                    titlePart1:"OurServices.Service",
                    titlePart2:"OurServices.Support",
                    icon:"headphone",
                    description:"OurServices.des"
                },
            ]
        }
    },
    
}
</script>
<style lang="">
    
</style>