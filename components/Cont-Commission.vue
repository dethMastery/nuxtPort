<template>
    <b-col cols="12" lg="9" class="rPart" style="padding: 0!important;">
        <!-- Heading IMG -->
        <div class="img-head">
            <div class="bs">
                <div class="head-text">
                    <h1>
                        Commission
                    </h1>
                </div>
            </div>
        </div>

        <!-- Comission Part -->
        <div class="Commission">
            <b-badge variant="warning">คำเตือน</b-badge> <span v-html="cont.Warning"></span>
            
            <br><br>

            <u>
                <h4>
                    Front-End Part
                </h4>
            </u>

            <br>

            <div v-for="fe in cont.FrontEndPart" :key="fe.id">
                <b-card no-body> 
                    <b-card-header v-b-toggle="'fe'+fe.id">
                        <span>
                            {{fe.title}}
                        </span>
                        <span style="float: right;">
                            <i class="fas fa-chevron-down"></i>
                        </span>
                    </b-card-header>
                    <b-collapse v-bind:id="'fe'+fe.id">
                        <b-card-body>
                            <b-row>
                                <b-col cols="8">
                                    <span v-html="fe.detailed"></span>
                                </b-col>
                                <b-col cols="4">
                                    <span>
                                        ราคา : {{fe.price}}
                                    </span>
                                    <br>
                                    <br>
                                    <span style="item-align: right;">
                                        <a :href="'mailto:'+mail" target="_blank">
                                            <b-button variant="success" class="d-block">
                                                กดเพื่อติดต่อ
                                            </b-button>
                                        </a>
                                    </span>
                                </b-col>

                                <b-col cols="12" class="text-center" v-if="fe.exampleLink != ' '">
                                    <a :href="fe.exampleLink" target="_blank">
                                        <img v-bind:src="fe.examplePic" :alt="fe.exampleText" style="width: 100%;">
                                    </a>
                                    <span>
                                        {{ fe.exampleText }}
                                    </span>
                                </b-col>
                            </b-row>
                        </b-card-body>
                    </b-collapse>
                </b-card>
            </div>
        </div>
    </b-col>
</template>

<script lang="ts">
    import axios from 'axios'

    export default {
        data() {
            return {
                cont: [],
                mail: "me@detzz.in.th"
            }
        },
        mounted() {
            axios
                .get('https://cdn.000198.xyz/api/prof')
                .then(response => (
                        this.cont = response.data.pF.Commission[0]
                    )
                )
        }
    }
</script>
