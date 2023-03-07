<template>
          <div class="our-blogs">
            <b-container >
                <!-- <b-row >
                    <b-col class="bg-info" cols="12" md="6" lg="4" >
                    <div class="blog">
                        <img src="" alt="">
                        <span>February 21, 2023</span>
                        <h3>The A to Z for Conversion <br>  of Android App to iOS App</h3>
                        <button>View Details <font-awesome-icon icon="fa-solid fa-arrow-right" /></button>
                    </div>
                    </b-col>
                </b-row> -->
                <h2 class="pt-5 pb-4">Our Blogs</h2>

                <carousel  autoplay="true" :nav="false" :dots="false" :responsive="{0:{items:1,nav:false},600:{items:3,nav:true}}">

                    <template v-for="item in 8">
                        <div class="blog">
                            <img src="~/assets/images/man-working-with-computer-side-view.png" alt="">
                            <div>
                                <span>February 21, 2023</span>
                                <h3>The A to Z for Conversion <br>  of Android App to iOS App</h3>
                                <button class="mb-4"><span><nuxt-link to="">View Details &nbsp;<font-awesome-icon icon="fa-solid fa-arrow-right" /></nuxt-link></span></button>
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

}
</script>
<style scoped>

</style>