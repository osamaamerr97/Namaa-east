<template lang="">
    <div class="footer py-5 text-white ">
        <b-container>
            <b-row class='mb-5'>
                <b-col sm='12' md='7' class='footer-logo'>
                    <img src="~/assets/images/logo.svg" alt="" style="Width:120px" srcset="">
                </b-col>
                <b-col sm='12' md='5'>
                    <div class="d-flex align-items-end justify-content-around h-100 footer-social">
                        <div class="footer-follow-us">
                            {{$t('Footer.Follow_Us')}}
                        </div>
                        <div>
                            <img src="~/assets/images/facebook.png" class=''  alt="">
                            <img src="~/assets/images/twitter.png" alt="">
                            <img src="~/assets/images/instagram.png" alt="">
                            <img src="~/assets/images/linkedin.png" alt="">
                        </div>
                    </div>
                </b-col>
            </b-row>
        </b-container>
        <hr>
        <b-container>
            <b-row class="pt-3">
                <b-col sm='12' md='5'>
                    <h4>{{$t('Footer.Newsletter')}}</h4>
                    <div class='description'>{{$t('Footer.des')}} <br> {{$t('Footer.update')}}</div>
                    <div class="newsletter-email "><form action="" @submit.prevent=""><input type='email' :placeholder="$t('Footer.Email_address')"/><button type='submit'>&nbsp;</button></form></div>
                </b-col>
                <b-col sm='12' md='3'>
                    <div class="">
                        <h4>{{$t('Footer.Company')}}</h4>
                        <ul>
                            <li class="mb-2"> <nuxt-link to=""> <font-awesome-icon icon="fa-solid fa-arrow-right"  /> &nbsp; {{$t('Footer.About_Us')}}</nuxt-link></li>
                            <li class="mb-2">  <nuxt-link to=""><font-awesome-icon icon="fa-solid fa-arrow-right"  /> &nbsp; {{$t('Footer.Contact')}}</nuxt-link></li>
                            <li class="mb-2">  <nuxt-link to=""><font-awesome-icon icon="fa-solid fa-arrow-right"  /> &nbsp; {{$t('Footer.Portfolio')}}</nuxt-link></li>
                            <li class="mb-2">  <nuxt-link to=""><font-awesome-icon icon="fa-solid fa-arrow-right"  /> &nbsp; {{$t('Footer.FAQ')}}</nuxt-link></li>
                            <li class="mb-2">  <nuxt-link to=""><font-awesome-icon icon="fa-solid fa-arrow-right"  /> &nbsp; {{$t('Footer.Blog')}}</nuxt-link></li>
                        </ul>
                    </div>
                </b-col>
                <b-col sm='12' md='3'>
                    <div class="">
                        <h4>{{$t('Footer.Services')}}</h4>
                        <ul>
                            <li class="mb-2"><nuxt-link to="">  <font-awesome-icon icon="fa-solid fa-arrow-right"  /> &nbsp; {{$t('Footer.Mobile_Development')}}</nuxt-link></li>
                            <li class="mb-2"> <nuxt-link to=""> <font-awesome-icon icon="fa-solid fa-arrow-right"  /> &nbsp; {{$t('Footer.Sales_Marketing')}}</nuxt-link></li>
                            <li class="mb-2"> <nuxt-link to=""> <font-awesome-icon icon="fa-solid fa-arrow-right"  /> &nbsp;{{$t('Footer.Design_Production')}}</nuxt-link></li>
                            <li class="mb-2"> <nuxt-link to=""> <font-awesome-icon icon="fa-solid fa-arrow-right"  /> &nbsp;{{$t('Footer.Web_Development')}}</nuxt-link></li>
                            <li class="mb-2"> <nuxt-link to=""> <font-awesome-icon icon="fa-solid fa-arrow-right"  /> &nbsp;{{$t('Footer.Service_Support')}}</nuxt-link></li>
                        </ul>
                    </div>
                </b-col>
            </b-row>


        </b-container>
    </div>
</template>
<script>
export default {
    
}
</script>
<style lang="">
    
</style>