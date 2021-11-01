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
                    console.log(response.data.Cert),
                    this.card = response.data.pF.Cert
                )
            )
    }
}
</script>