<template>
    <b-col cols="12" lg="9" class="rPart" style="padding: 0!important;">
        <!-- Heading IMG -->
        <div class="img-head">
            <div class="bs">
                <div class="head-text">
                    <h1>
                        Works
                    </h1>
                </div>
            </div>
        </div>

        <!-- Works Part -->
        <div class="works">
            <div class="card-holder row"> 
                <div class="cloak col-12 col-sm-6 col-md-4 p-0 p-2">
                    <div class="card h-100">
                        <a href="#working" class="card-img-wrap" data-bs-toggle="modal" data-bs-target="#working-2-b">
                            <img class="card-img-top" v-bind:src="cardImg0">
                        </a>
                        <div class="card-body">
                            <h5 class="card-title">
                                <strong>
                                    {{cardTitle0}}
                                </strong>
                            </h5>
                        </div>
                        <div class="card-footer">
                            <p class="card-text" style="text-align: right">
                                {{cardDate0}}
                            </p>
                        </div>
                    </div>
                </div>
              
            </div>
        </div>
    </b-col>
</template>

<script>
import axios from 'axios'

export default {
    data() {
        return {
            cardImg0: null,
            cardTitle0: null,
            cardDate0: null,

            cardImg1: null,
            cardTitle1: null,
            cardDate1: null,

            cardImg2: null,
            cardTitle2: null,
            cardDate2: null,

            cardImg3: null,
            cardTitle3: null,
            cardDate3: null,

            cardImg4: null,
            cardTitle4: null,
            cardDate4: null
        }
    },
    mounted() {
        axios
            .get('https://raw.githubusercontent.com/dethMastery/nuxtPort/%E0%B9%80%E0%B8%82%E0%B8%B2%E0%B9%80%E0%B8%82%E0%B8%B5%E0%B8%A2%E0%B8%A7%F0%9F%97%BB/components/db/database.json')
            .then(response => (
                    this.cardImg0 = response.data.Work[0].pix,
                    this.cardTitle0 = response.data.Work[0].title,
                    this.cardDate0 = response.data.Work[0].date,

                    this.cardImg1 = response.data.Work[1].pix,
                    this.cardTitle1 = response.data.Work[1].title,
                    this.cardDate1 = response.data.Work[1].date,

                    this.cardImg2 = response.data.Work[2].pix,
                    this.cardTitle2 = response.data.Work[2].title,
                    this.cardDate2 = response.data.Work[2].date,

                    this.cardImg3 = response.data.Work[3].pix,
                    this.cardTitle3 = response.data.Work[3].title,
                    this.cardDate3 = response.data.Work[3].date,

                    this.cardImg4 = response.data.Work[4].pix,
                    this.cardTitle4 = response.data.Work[4].title,
                    this.cardDate4 = response.data.Work[4].date
                )
            )
    }
}
</script>