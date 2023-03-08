<template>
    <div>
        <b-container class="contact mt-5 pt-5">
                <b-row class="">
   
                    <b-col class="" cols="12" md="6">
                        <div class="contact-info">
                            <h2>{{$t('contact.start')}} <br>  <span> {{$t('contact.journey')}}</span></h2>

                            <div>
                                <img src="phone-call.png" alt="">
                                <span>+966507108581</span>
                            </div>
                            <div>
                                <img src="email.png" alt="">
                                <span>support@namaaalsharq.sa</span>
                            </div>
                            <div>
                                <img src="marker.svg" alt="">
                                <span>+966507108581</span>
                            </div>
                        </div>
                    </b-col>

                    <b-col class="" cols="12" md="6" >
                        <div  class="form">
                          
                            <b-form>
                                <b-form-group  v-for="type in types"  :key="type.type" :class="type.width" class="mb-3"  label="Enter your name"        :label-for="`type-${type.type}`"
>
                                    <b-form-input 
                                    size="lg"
                                    :id="`type-${type.type}`"
                                    :type="type.type" 
                                    ></b-form-input>
                                    
                                </b-form-group>





                                <!-- <b-input-group >
                                    <b-input-group-prepend size="lg" is-text>
                                        <font-awesome-icon icon="fa-solid fa-user" class="bg-white text-dark w-50 "/>
                                    </b-input-group-prepend>
                                    <b-form-input   type="email" placeholder="me@example.com"></b-form-input>
                                </b-input-group> -->
                            </b-form>
                        </div>
                    </b-col>
                </b-row>
            </b-container>
    </div>
</template>
<script>
export default {
    data() {
      return {
        types: [
            {
                type:'text',
                placeholder:"User name",
                width:'w-45 d-inline-block'
            },
            {
                type:'text',
                placeholder:"Last name",
                width:'w-45  d-inline-block ml'
            },
            {
                type:'email',
                placeholder:"Email",
                width:'w-100'
            },
            {
                type:'number',
                placeholder:"Phone number",
                width:'w-100'
            },
        ]
      }
    }
}
</script>
<style scoped>
.w-45{
    width: 48%;

}
.ml{
    margin-left: 4%;

}    
</style>