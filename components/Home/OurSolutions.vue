<template>
    <div class="our-solutions">
        <b-container class="solutions-container">
            <h2>{{ $t('OurSolutions.Our') }} <span>{{ $t('OurSolutions.Solutions') }}</span>  {{ $t('OurSolutions.Section') }}</h2>
            <b-row>
                <b-col sm="12" md="4">
                    <div>
                        <ul class="solutions-list">
                            <li :class="{'active':activeClass[0].isActive}" @click="howOurSolutionDetails(
                                {
                                    head:'OurSolutions.ERP_Modules',
                                    l1:'OurSolutions.Accounting_software',
                                    l2:'OurSolutions.HR_software',
                                    l3:'OurSolutions.Inventory_management_software',
                                    l4:'OurSolutions.Project_management_software',
                                    l5:'OurSolutions.Real_estate_ERP',
                                    imgSrc:'kaitlyn-baker-vZJdYl5JVXY-unsplash@2x.png',
                                    viewDetailsLink:'ERP_Modules',
                                    isActive:'isERPModulesActive'
                                }
                            )">
                            {{ $t('OurSolutions.l1') }}
                            </li>
                            <li :class="{'active':activeClass[1].isActive}"  @click="howOurSolutionDetails(
                                {
                                    head:'OurSolutions.E_Learning',
                                    l1:'OurSolutions.Accounting_software',
                                    l2:'OurSolutions.HR_software',
                                    l3:'OurSolutions.Inventory_management_software',
                                    l4:'OurSolutions.Project_management_software',
                                    l5:'OurSolutions.Real_estate_ERP',
                                    imgSrc:'310949071_433594378881558_4432399218514107525_n.png',
                                    viewDetailsLink:'E_Learning',
                                    isActive:'isELearningActive'
                                }
                            )">
                            {{ $t('OurSolutions.l2') }}
                            </li>
                            <li :class="{'active':activeClass[2].isActive}"  @click="howOurSolutionDetails(
                                {
                                    head:'OurSolutions.Service_Procurement',
                                    l1:'OurSolutions.Accounting_software',
                                    l2:'OurSolutions.HR_software',
                                    l3:'OurSolutions.Inventory_management_software',
                                    l4:'OurSolutions.Project_management_software',
                                    l5:'OurSolutions.Real_estate_ERP',
                                    imgSrc:'kaitlyn-baker-vZJdYl5JVXY-unsplash@2x.png',
                                    viewDetailsLink:'E_Learning',
                                    isActive:'isServiceProcurementActive'
                                }
                            )">
                            {{ $t('OurSolutions.l3') }}
                            </li>
                            <li :class="{'active':activeClass[3].isActive}"  @click="howOurSolutionDetails(
                                {
                                    head:'OurSolutions.Logistics',
                                    l1:'OurSolutions.Accounting_software',
                                    l2:'OurSolutions.HR_software',
                                    l3:'OurSolutions.Inventory_management_software',
                                    l4:'OurSolutions.Project_management_software',
                                    l5:'OurSolutions.Real_estate_ERP',
                                    imgSrc:'Component 27 – 1.png',
                                    viewDetailsLink:'E_Learning',
                                    isActive:'isLogisticsActive'
                                }
                            )">
                            {{ $t('OurSolutions.l4') }}
                            </li>
                            <li :class="{'active':activeClass[4].isActive}"  @click="howOurSolutionDetails(
                                {
                                    head:'OurSolutions.E-Commerce',
                                    l1:'OurSolutions.Accounting_software',
                                    l2:'OurSolutions.HR_software',
                                    l3:'OurSolutions.Inventory_management_software',
                                    l4:'OurSolutions.Project_management_software',
                                    l5:'OurSolutions.Real_estate_ERP',
                                    imgSrc:'Mask Group 42.png',
                                    viewDetailsLink:'E_Learning',
                                    isActive:'isECommerceActive'
                                }
                            )">
                            {{ $t('OurSolutions.l5') }}
                            </li>
                            <li :class="{'active':activeClass[5].isActive}"  @click="howOurSolutionDetails(
                                {
                                    head:'OurSolutions.Tourism',
                                    l1:'OurSolutions.Accounting_software',
                                    l2:'OurSolutions.HR_software',
                                    l3:'OurSolutions.Inventory_management_software',
                                    l4:'OurSolutions.Project_management_software',
                                    l5:'OurSolutions.Real_estate_ERP',
                                    imgSrc:'man-working-with-computer-side-view.png',
                                    viewDetailsLink:'E_Learning',
                                    isActive:'isTourismActive'
                                }
                            )">
                            {{ $t('OurSolutions.l6') }}
                            </li>
                            <li :class="{'active':activeClass[6].isActive}"  @click="howOurSolutionDetails(
                                {
                                    head:'OurSolutions.Nonprofit',
                                    l1:'OurSolutions.Accounting_software',
                                    l2:'OurSolutions.HR_software',
                                    l3:'OurSolutions.Inventory_management_software',
                                    l4:'OurSolutions.Project_management_software',
                                    l5:'OurSolutions.Real_estate_ERP',
                                    imgSrc:'Mask Group 100.png',
                                    viewDetailsLink:'E_Learning',
                                    isActive:'isNonprofitActive'
                                }
                            )">
                            {{ $t('OurSolutions.l7') }}
                            </li>
                            <li :class="{'active':activeClass[7].isActive}"  @click="howOurSolutionDetails(
                                {
                                    head:'OurSolutions.Entertainment',
                                    l1:'OurSolutions.Accounting_software',
                                    l2:'OurSolutions.HR_software',
                                    l3:'OurSolutions.Inventory_management_software',
                                    l4:'OurSolutions.Project_management_software',
                                    l5:'OurSolutions.Real_estate_ERP',
                                    imgSrc:'Mask Group 98.png',
                                    viewDetailsLink:'E_Learning',
                                    isActive:'isEntertainmentActive'
                                }
                            )">
                            {{ $t('OurSolutions.l8') }}
                            </li>
                            <li :class="{'active':activeClass[8].isActive}"  @click="howOurSolutionDetails(
                                {
                                    head:'OurSolutions.Transportation',
                                    l1:'OurSolutions.Accounting_software',
                                    l2:'OurSolutions.HR_software',
                                    l3:'OurSolutions.Inventory_management_software',
                                    l4:'OurSolutions.Project_management_software',
                                    l5:'OurSolutions.Real_estate_ERP',
                                    imgSrc:'Mask Group 44.png',
                                    viewDetailsLink:'E_Learning',
                                    isActive:'isTransportationActive'
                                }
                            )">
                            {{ $t('OurSolutions.l9') }}
                            </li>
                            <li :class="{'active':activeClass[9].isActive}"  @click="howOurSolutionDetails(
                                {
                                    head:'OurSolutions.Personal_Care_&_Wellness',
                                    l1:'OurSolutions.Accounting_software',
                                    l2:'OurSolutions.HR_software',
                                    l3:'OurSolutions.Inventory_management_software',
                                    l4:'OurSolutions.Project_management_software',
                                    l5:'OurSolutions.Real_estate_ERP',
                                    imgSrc:'header-bacground.png',
                                    viewDetailsLink:'E_Learning',
                                    isActive:'isPersonalCareWellnessActive'
                                }
                            )">
                            {{ $t('OurSolutions.l10') }}
                            </li>
                            <li :class="{'active':activeClass[10].isActive}"  @click="howOurSolutionDetails(
                                {
                                    head:'OurSolutions.Cloud_Based_Solutions',
                                    l1:'OurSolutions.Accounting_software',
                                    l2:'OurSolutions.HR_software',
                                    l3:'OurSolutions.Inventory_management_software',
                                    l4:'OurSolutions.Project_management_software',
                                    l5:'OurSolutions.Real_estate_ERP',
                                    imgSrc:'kaitlyn-baker-vZJdYl5JVXY-unsplash.png',
                                    viewDetailsLink:'E_Learning',
                                    isActive:'isCloudBasedSolutionsActive'
                                }
                            )">
                            {{ $t('OurSolutions.l11') }}
                            </li>

                        </ul>
                    </div>
                </b-col>
                <b-col sm="12" md="8">
                    <div class="soultion-details">
                        <div class="soultion-details-content">
                            <h2>
                                {{OurSolutionsDetails.head}}
                            </h2>
                            <ul>
                                <li>
                                    {{OurSolutionsDetails.l1}}

                                </li>
                                <li>
                                    {{OurSolutionsDetails.l2}}

                                </li>
                                <li>
                                    {{OurSolutionsDetails.l3}}

                                </li>
                                <li>

                                    {{OurSolutionsDetails.l4}}
                                </li>
                                <li>
                                    {{OurSolutionsDetails.l5}}
                                    
                                </li>
                            </ul>

                            <button class="mb-4"><span><nuxt-link :to="OurSolutionsDetails.viewDetailsLink">{{ $t('OurSolutions.View_Details') }} &nbsp;<font-awesome-icon v-if="currentLang=='en'" icon="fa-solid fa-arrow-right" /><font-awesome-icon v-else icon="fa-solid fa-arrow-left" /></nuxt-link></span></button>

                        </div>
                        <div class="soultion-details-img">
                            <img :src="OurSolutionsDetails.imgSrc" alt="" class=""  srcset="">

                            <!-- {{OurSolutionsDetails.imgSrc}} -->
                        </div>
                    </div>
                </b-col>
            </b-row>
        </b-container>
    </div>
</template>
<script>
export default {
    name:"our-solutions",
    data() {
        return {
            OurSolutionsDetails:{
                head:this.$t('OurSolutions.ERP_Modules'),
                l1:this.$t('OurSolutions.Accounting_software'),
                l2:this.$t('OurSolutions.HR_software'),
                l3:this.$t('OurSolutions.Inventory_management_software'),
                l4:this.$t('OurSolutions.Project_management_software'),
                l5:this.$t('OurSolutions.Real_estate_ERP'),
                imgSrc:'kaitlyn-baker-vZJdYl5JVXY-unsplash@2x.png',
                viewDetailsLink:'link',
            },
            activeClass:[
                
            {
                name:'isERPModulesActive',
                isActive:true
            },
            {
                name:'isELearningActive',
                isActive:false
            },
            {
                name:'isServiceProcurementActive',
                isActive:false
            },
            {
                name:'isLogisticsActive',
                isActive:false
            },
            {
                name:'isECommerceActive',
                isActive:false
            },
            {
                name:'isTourismActive',
                isActive:false
            },
            {
                name:'isNonprofitActive',
                isActive:false
            },
            {
                name:'isEntertainmentActive',
                isActive:false
            },
            {
                name:'isTransportationActive',
                isActive:false
            },
            {
                name:'isPersonalCareWellnessActive',
                isActive:false
            },
            {
                name:'isCloudBasedSolutionsActive',
                isActive:false
            },
        ]
        }
    },
    computed:{
        currentLang(){
            return this.$i18n.locale
        },

    },
    methods:{
        howOurSolutionDetails(data){
            this.OurSolutionsDetails.head= this.$t(data.head)
            this.OurSolutionsDetails.l1= this.$t(data.l1)
            this.OurSolutionsDetails.l2= this.$t(data.l2)
            this.OurSolutionsDetails.l3= this.$t(data.l3)
            this.OurSolutionsDetails.l4= this.$t(data.l4)
            this.OurSolutionsDetails.l5= this.$t(data.l5)
            this.OurSolutionsDetails.imgSrc= data.imgSrc
            this.OurSolutionsDetails.viewDetailsLink= this.$t(data.viewDetailsLink)

            for(let i =0 ; i < this.activeClass.length;i++){
               if( this.activeClass[i].name == data.isActive){
                    this.activeClass[i].isActive = true
                }else{                    
                    this.activeClass[i].isActive = false
                }

            }
            

        }
    }
}
</script>
<style lang="">
    
</style>