<template>
          <div class="our-blogs">
            <b-container >
                <h2 class="pt-5 pb-4">{{$t('oueBlogs.our_blogs')}}</h2>

                <carousel  autoplay="true" :nav="false" :dots="false" :responsive="{0:{items:1,nav:false},600:{items:3,nav:true}}">

                    <template v-for="item in 8">
                        <div class="blog">
                            <img src="~/assets/images/man-working-with-computer-side-view.png" alt="">
                            <div>
                                <span>{{$t('oueBlogs.date')}}</span>
                                <h3>{{$t('oueBlogs.des1')}} <br> {{$t('oueBlogs.des2')}}</h3>
                                <button class="mb-4"><span><nuxt-link to="">{{ $t('oueBlogs.View_Details') }} &nbsp;<font-awesome-icon v-if="currentLang=='en'" icon="fa-solid fa-arrow-right" /><font-awesome-icon v-else icon="fa-solid fa-arrow-left" /></nuxt-link></span></button>
                            </div>
                        </div>                        
                    </template>

                </carousel>
                
            </b-container>
        </div>
</template>
<script>

export default {
    name:'our-blogs',
    computed:{
        currentLang(){
            return this.$i18n.locale
        },

    },
}
</script>
<style scoped>

</style>