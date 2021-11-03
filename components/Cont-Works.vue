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
            <b-row style="width: 100%; !important">
                <div v-for="info in card" :key="info.id" class="col-12 col-md-6 pr-1 pb-2">
                    <div class="card h-100">
                        <a href="/" class="card-img-wrap" v-b-modal="'mod'+info.id">
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

            <div v-for="info in card" :key="info.id">
                <b-modal :id="'mod'+info.id" :title="info.title" hide-footer>
                    <img :src="info.pix" :alt="info.title" class="img-modal">
                </b-modal>
            </div>

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
            .get('https://cdn.000198.xyz/api/prof')
            .then(response => (
                    console.log(response.data.Work),
                    this.card = response.data.pF.Work
                )
            )
    }
}
</script>