<template>
    <b-col cols="12" lg="9" class="rPart" style="padding: 0!important;">
        <!-- Heading IMG -->
        <div class="img-head">
            <div class="bs">
                <div class="head-text">
                    <h1>
                        Contact
                    </h1>
                </div>
            </div>
        </div>

        <!-- Cert Part -->
        <div class="Contact">

            <b-card no-body v-for="contact in cont" :key="contact.id" class="col-12">
                <b-card-header v-b-toggle="'cont'+contact.id">
                    <span id="cTitle">
                        {{contact.index}}
                    </span>
                    <span style="float: right;">
                        <i class="fas fa-chevron-down"></i>
                    </span>
                </b-card-header>
                <b-collapse :id="'cont'+contact.id">
                    <b-card-body class="text-center">
                        <a class="s-button" :href="contact.link" target="_blank">
                            <span class="logo" :style="'background: '+contact.bgColor+';'">
                                <i :class="'fi '+ contact.icon" :style="'color :'+contact.iColor+'; padding: '+contact.iPadd+';'"></i>
                            </span>
                            <span class="text" :style="'font-size:' + contact.fsize + ';'">
                                {{contact.data}}
                            </span>
                        </a>
                    </b-card-body>
                </b-collapse>
            </b-card>

        </div>
    </b-col>
</template>

<script>
import axios from 'axios'

export default {
    data() {
        return {
            cont: []
        }
    },
    mounted() {
        axios.get('https://cdn.000198.xyz/api/prof')
             .then(response => (
                 this.cont = response.data.pF.Contact
                )
             )
    }
}
</script>