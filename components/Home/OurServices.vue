<template>
    <div>
        <div class="our-services">
            <b-container class="bv-example-row mt-5 pt-5">
                <b-row class="">
                    <b-col class="colum" cols="12" md="6" lg="4" >
                    <div class="d-flex align-items-center h-100">
                        <h2><span>Our </span> <br> Services</h2>
                    </div>
                    </b-col>
                    <b-col class="colum" v-for="service in services" :key="service.titlePart1" cols="12" md="6" lg="4" >
                    <div class="service">
                        <div class="service-title d-flex align-items-center justify-content-between">
                        <h4>{{service.titlePart1}} <br> {{service.titlePart2}}</h4>
                        <div>{{service.icon}}</div>
                        </div>
                        <div class="service-description"> {{service.description}}</div>
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
                    titlePart1:"Application",
                    titlePart2:"Development",
                    icon:"icon",
                    description:"We are experts in iOS and Android native development, as well as React Native."
                },
                {
                    titlePart1:"Consulting & ",
                    titlePart2:"Advisory",
                    icon:"icon",
                    description:"We are experts in iOS and Android native development, as well as React Native."
                },
                {
                    titlePart1:"Design & ",
                    titlePart2:"Production",
                    icon:"icon",
                    description:"We are experts in iOS and Android native development, as well as React Native."
                },
                {
                    titlePart1:"Sales & ",
                    titlePart2:"Marketing",
                    icon:"icon",
                    description:"We are experts in iOS and Android native development, as well as React Native."
                },
                {
                    titlePart1:"Service &  ",
                    titlePart2:"Support",
                    icon:"icon",
                    description:"We are experts in iOS and Android native development, as well as React Native."
                },
            ]
        }
    },
    
}
</script>
<style lang="">
    
</style>