<template>
    <b-col cols="12" lg="9" class="rPart" style="padding: 0!important;">
        <!-- Heading IMG -->
        <div class="img-head">
            <div class="bs">
                <div class="head-text">
                    <h1>
                        About
                    </h1>
                </div>
            </div>
        </div>

        <!-- Info Part -->
        <div class="Info">
            <h3 class="infoHeader">
                <u>
                    Who Am I?
                </u>
            </h3>
            <ul>
                <li>
                    <h5>
                        Name : {{add.name}}
                    </h5>
                </li>

                <li>
                    <h5>
                        Age : {{age}}
                    </h5>
                </li>

                <li>
                    <h5>
                        Education Profile : {
                    </h5>
                        <ul>
                            <li v-for="sc in edu" :key="sc.id">
                                {{sc.grade}} -> {{sc.subj}} [{{sc.year}}]
                            </li>
                        </ul>
                    <h5>
                        }
                    </h5>
                </li>
            </ul>
        </div>
    </b-col>
</template>

<script>
    import axios from 'axios'

    // var agg = new Date().getFullYear() - new Date(this.add.birthDate).getFullYear()

    export default {
        data() {
            return {
                add: [],
                edu: [],
                age: null
            }
        },
        mounted() {
            axios
                .get('https://cdn.000198.xyz/api/prof')
                .then(response => (
                    this.add = response.data.pF.About[0],
                    this.edu = response.data.pF.About[0].Edu,
                    console.log(new Date().getFullYear()),
                    console.log(new Date(this.add.birthDate).getFullYear()),
                    this.age = new Date().getFullYear() - new Date(this.add.birthDate).getFullYear()
                )
            )
        }
    }
    
</script>