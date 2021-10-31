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
            <b-row style="width: 100%;! important">
                <div v-for="info in card" :key="info.id" class="col-12 col-md-6 pr-1 pb-2">
                    <div class="card h-100">
                        <a href="#working" class="card-img-wrap" data-bs-toggle="modal" data-bs-target="#working-2-b">
                            <img class="card-img-top" v-bind:src="info.pix">
                        </a>
                        <div class="card-body">
                            <h5 class="card-title">
                                <strong>
                                    {{info.title}}
                                </strong>
                            </h5>
                        </div>
                        <div class="card-footer">
                            <p class="card-text" style="text-align: right">
                                {{info.date}}
                            </p>
                        </div>
                    </div>
                </div>
            </b-row>
        </div>
    </b-col>
</template>

<script>
import axios from 'axios'

export default {
    data() {
        return {
            card: []
        }
    },
    mounted() {
        axios
            .get('https://raw.githubusercontent.com/dethMastery/nuxtPort/%E0%B9%80%E0%B8%82%E0%B8%B2%E0%B9%80%E0%B8%82%E0%B8%B5%E0%B8%A2%E0%B8%A7%F0%9F%97%BB/components/db/database.json')
            .then(response => (
                    console.log(response.data.Work),
                    this.card = response.data.Work
                )
            )
    }
}
</script>