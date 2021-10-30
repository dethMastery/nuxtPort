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
            <h3>
                Who Am I?
            </h3>
            <br>
            <ul>
                <li>
                    <h5>
                        Name : <span id="Name"></span>
                    </h5>
                </li>

                <li>
                    <h5>
                        Age : <span id="Age"></span>
                    </h5>
                </li>

                <li>
                    <h5>
                        Education Profile : {
                    </h5>
                        <ul id="EdProf">
                        </ul>
                    <h5>
                        }
                    </h5>
                </li>
            </ul>
        </div>
    </b-col>
</template>