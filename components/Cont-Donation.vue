<template>
    <b-col cols="12" lg="9" class="rPart" style="padding: 0!important;">
        <!-- Heading IMG -->
        <div class="img-head">
            <div class="bs">
                <div class="head-text">
                    <h1>
                        Donation
                    </h1>
                </div>
            </div>
        </div>

        <!-- Info Part -->
        <div class="Donation">
            <b-row>
                <div block v-for="dn in donate" :key="dn.id" class="col-12 col-lg-4">
                    <a :href="dn.link" v-if="dn.type != 'expanded' " class="donateD">
                        <b-button block :style="'background: '+ dn.bgcolor + '; border: 0; color: ' + dn.tcolor + ';'">
                            <i :class="dn.icon"></i>
                            &nbsp;
                            <span>
                                {{dn.name}}
                            </span>
                        </b-button>
                    </a>
                    
                    <b-button block :style="'background: '+ dn.bgcolor + '; border: 0; color: ' + dn.tcolor + ';'" v-if="dn.type != 'button'" v-b-toggle="'dn'+dn.id">
                        <i :class="dn.icon"></i>
                        &nbsp;
                        <span>
                            {{dn.name}}
                        </span>
                    </b-button>
                    <c-col cols="12" class="d-block d-md-block d-lg-none">
                        <br>
                    </c-col>
                </div>
            </b-row>

            <br>

            <div block v-for="dn in donate" :key="dn.id" class="col-12">
                <b-collapse :id="'dn'+dn.id">
                    <b-card no-body class="mb-2">
                        <b-card-header>
                            {{dn.name}}
                        </b-card-header>
                        <b-card-body class="text-center">
                            <span v-html="dn.detailed"></span>
                            <a :href="dn.link" v-if="dn.link != ' '">
                                Link
                            </a>
                        </b-card-body>
                    </b-card>
                </b-collapse>
            </div>
        </div>
    </b-col>
</template>

<script>
import axios from 'axios'

export default {
    data() {
        return {
            donate: []
        }
    },
    mounted() {
        axios.get('https://cdn.000198.xyz/api/prof')
             .then(response => (
                 this.donate = response.data.pF.Donation
                )
             )
    }
}
</script>