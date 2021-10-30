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
                        Name : {{ name }}
                    </h5>
                </li>

                <li>
                    <h5>
                        Age : {{ age }}
                    </h5>
                </li>

                <li>
                    <h5>
                        Education Profile : {
                    </h5>
                        <ul>
                            <li>
                                {{Edu1}}
                            </li>
                            <li>
                                {{Edu2}}
                            </li>
                            <li>
                                {{Edu3}}
                            </li>
                            <li>
                                {{Edu4}}
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

<script lang="ts">
    var name = "Suphakit Pinyoworapot"
    var birthDate = "June 15, 2002"

    var g1 = "Grade 11-12"
    var g2 = "Grade 10"
    var g3 = "Grade 7-9"
    var g4 = "Kintergarden - Grade 6"

    var s1 = "[Math-Sci] Darasamutr Sriracha School"
    var s2 = "[Math-Sci] Piboonbumpen Demonstration School"
    var s3 = "[MEP] Sriracha School"
    var s4 = "Darasamutr Sriracha School"

    var y1 = "2019 - April 2021"
    var y2 = "2018 - 2019"
    var y3 = "2014 - 2018"
    var y4 = "2005 - 2014"

    var d = new Date(birthDate)
    var bd = d.getFullYear()
    var x = new Date()
    var n = x.getFullYear()
    var p = n - bd

    var e1 =  g1 + ' -> ' + s1 + ' [ ' + y1 + ' ]'
    var e2 =  g2 + ' -> ' + s2 + ' [ ' + y2 + ' ]'
    var e3 =  g3 + ' -> ' + s3 + ' [ ' + y3 + ' ]'
    var e4 =  g4 + ' -> ' + s4 + ' [ ' + y4 + ' ]'

    export default {
        data() {
            return {
                name : name,
                age: p,
                Edu1: e1,
                Edu2: e2,
                Edu3: e3,
                Edu4: e4,
            }
        },
    }
</script>