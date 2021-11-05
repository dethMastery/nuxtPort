<template>
    <b-col cols="12" lg="9" class="rPart" style="padding: 0!important;">
        <b-carousel
            id="carousel-1"
            indicators
            controls
            >     
            <b-carousel-slide v-for="pic in home" :key="pic.id">
                <template #img>
                    <div :style="'background-image: url(' + pic.bg + ');'" class="carousel-img img">
                        <div class="blackscreen"></div>
                    </div>
                    <div class="carousel-caption">
                        <h5>
                            {{pic.heading}}
                        </h5>
                        <p>
                            {{pic.subhead}}
                        </p>
                    </div>
                </template>
            </b-carousel-slide>
        </b-carousel>
    </b-col>
</template>

<style>
    .img {
        background-image: url('https://box.lolis.love/0/hflzv.webp');
        width: 100%;
        height: 100%;
        background-size: cover;
        background-position: center;
    }
</style>

<script>
import axios from 'axios'

export default {
    data() {
        return {
            home: []
        }
    },
    mounted() {
        axios.get('https://cdn.000198.xyz/api/prof')
             .then(response => (
                 this.home = response.data.pF.Home
                )
             )
    }
}
</script>