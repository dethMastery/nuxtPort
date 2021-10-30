<template>
    <b-col cols="12" lg="9" class="rPart" style="padding: 0!important;">
        <!-- Header IMG -->
        <div class="img-head">
            <div class="bs">
                <div class="head-text">
                    <h1>
                        Skills
                    </h1>
                </div>
            </div>
        </div>

        <!-- Skill Part -->
        <div class="Skill">
            <h5>
                <b>
                    Front-End Web Devolopment
                </b>
            </h5>
            <b-progress :max="max">
                <b-progress-bar class="html" :value="values[0]" animated show-progress>
                    HTML
                </b-progress-bar>
                <b-progress-bar class="css" :value="values[1]" animated show-progress>
                    CSS
                </b-progress-bar>
                <b-progress-bar class="jsF" :value="values[2]" animated show-progress>
                    JS Framework
                </b-progress-bar>
            </b-progress>
            <br/>
            <h5>
                <b>
                    Back-End Web Development
                </b>
            </h5>
            <b-progress :max="max">
                <b-progress-bar class="php" :value="values[3]" animated show-progress>
                    PHP
                </b-progress-bar>
                <b-progress-bar class="js" :value="values[4]" animated show-progress>
                    JavaScript
                </b-progress-bar>
                <b-progress-bar class="ts" :value="values[5]" animated show-progress>
                    TypeScript
                </b-progress-bar>
            </b-progress>
            <br>

            <h5>
                <b>
                    Music Production
                </b>
            </h5>
            <b-progress :max="max">
                <b-progress-bar class="master" :value="values[6]" animated show-progress>
                    Mastering
                </b-progress-bar>
                <b-progress-bar class="sing" :value="values[7]" variant="info" animated show-progress>
                    Singing
                </b-progress-bar>
                <b-progress-bar class="prod" :value="values[8]" animated show-progress>
                    Producing
                </b-progress-bar>
                <b-progress-bar class="comp" :value="values[9]" animated show-progress>
                    Composing
                </b-progress-bar>
            </b-progress>
        </div>
    </b-col>
</template>

<script>
  export default {
    data() {
      return {
        values: [25,40,35, 40,35,25, 10,20,40,30],
        max: 100
      }
    }
  }
</script>