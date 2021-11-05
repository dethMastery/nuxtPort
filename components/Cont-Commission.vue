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

            <!-- FrontEnd -->
            <u>
                <h4>
                    Front-End
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
                                <b-col>
                                    <br>
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

            <!--Music -->
            <u>
                <h4>
                    Music
                </h4>
            </u>
            <br>
            <div v-for="m in cont.MusicPart" :key="m.id">
                <b-card no-body> 
                    <b-card-header v-b-toggle="'m'+m.id">
                        <span>
                            {{m.title}}
                        </span>
                        <span style="float: right;">
                            <i class="fas fa-chevron-down"></i>
                        </span>
                    </b-card-header>
                    <b-collapse v-bind:id="'m'+m.id">
                        <b-card-body>
                            <b-row>
                                <b-col cols="8">
                                    <span v-html="m.detailed"></span>
                                </b-col>
                                <b-col cols="4">
                                    <span>
                                        ราคา : {{m.price}}
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
                                <b-col>
                                    <br>
                                </b-col>
                                <b-col cols="12" class="text-center" v-if="m.exampleLink != ' '">
                                    <a :href="m.exampleLink" target="_blank">
                                        <img v-bind:src="m.examplePic" :alt="m.exampleText" style="width: 100%;">
                                    </a>
                                    <span>
                                        {{ m.exampleText }}
                                    </span>
                                </b-col>
                            </b-row>
                        </b-card-body>
                    </b-collapse>
                </b-card>
            </div>

            <!-- Video -->
            <u>
                <h4>
                    Video
                </h4>
            </u>
            <br>
            <div v-for="vid in cont.VideoPart" :key="vid.id">
                <b-card no-body> 
                    <b-card-header v-b-toggle="'vid'+vid.id">
                        <span>
                            {{vid.title}}
                        </span>
                        <span style="float: right;">
                            <i class="fas fa-chevron-down"></i>
                        </span>
                    </b-card-header>
                    <b-collapse v-bind:id="'vid'+vid.id">
                        <b-card-body>
                            <b-row>
                                <b-col cols="8">
                                    <span v-html="vid.detailed"></span>
                                </b-col>
                                <b-col cols="4">
                                    <span>
                                        ราคา : {{vid.price}}
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
                                <b-col>
                                    <br>
                                </b-col>
                                <b-col cols="12" class="text-center" v-if="vid.exampleLink != ' '">
                                    <a :href="vid.exampleLink" target="_blank">
                                        <img v-bind:src="vid.examplePic" :alt="vid.exampleText" style="width: 100%;">
                                    </a>
                                    <span>
                                        {{ vid.exampleText }}
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

<script>
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
