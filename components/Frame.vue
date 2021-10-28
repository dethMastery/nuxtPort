<template>
    <b-container fluid>
        <b-row>
            <!-- Navbar -->
                <b-col cols="12" class="mNav d-block d-lg-none d-xl-none d-md-block w-100">
                    <b-navbar toggleable="lg" type="dark">
                        <b-navbar-brand href="#">Suphakit P.</b-navbar-brand>

                        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

                        <b-collapse id="nav-collapse" style="text-align: center;" is-nav>
                            <b-navbar-nav>
                                <b-nav-item href="/">
                                    Home
                                </b-nav-item>
                                <b-nav-item href="/About">
                                    About
                                </b-nav-item>
                                <b-nav-item href="/Skill">
                                    Skill
                                </b-nav-item>
                                <b-nav-item href="/Works">
                                    Works
                                </b-nav-item>
                                <b-nav-item href="/Cert">
                                    Certificate
                                </b-nav-item>
                                <b-nav-item href="/Commission">
                                    Commission
                                </b-nav-item>
                                <b-nav-item href="/Contact">
                                    Contact
                                </b-nav-item>
                                <b-nav-item href="/Donation">
                                    Donation
                                </b-nav-item>
                            </b-navbar-nav>
                        </b-collapse>
                    </b-navbar>

                </b-col>

            <!-- Left -->
                <b-col cols="12" md="3" class="lPart d-sm-none d-md-none d-lg-block d-none">
                    <h1 class="lHeader">
                        Portfolio
                    </h1>

                    <center>
                        <div class="lIMG-Holder">
                            <img src="https://nc.detzz.in.th/img/prof.webp" alt="Profile" class="lIMG" />
                        </div>
                    </center>

                    <div class="lMenu">
                        <br />
                        <br />
                        <b-nav vertical>
                            <b-nav-item href="/" class="lNavLink">
                                <h5>
                                    Home
                                </h5>
                            </b-nav-item>
                            <b-nav-item href="/About" class="lNavLink">
                                <h5>
                                    About
                                </h5>
                            </b-nav-item>
                            <b-nav-item href="/Skill" class="lNavLink">
                                <h5>
                                    Skill
                                </h5>
                            </b-nav-item>
                            <b-nav-item href="/Works" class="lNavLink">
                                <h5>
                                    Works
                                </h5>
                            </b-nav-item>
                            <b-nav-item href="/Cert" class="lNavLink">
                                <h5>
                                    Certificates
                                </h5>
                            </b-nav-item>
                            <b-nav-item href="/Commission" class="lNavLink">
                                <h5>
                                    Commission
                                </h5>
                            </b-nav-item>
                            <b-nav-item href="/Contact" class="lNavLink">
                                <h5>
                                    Contact
                                </h5>
                            </b-nav-item>
                            <b-nav-item href="/Donation" class="lNavLink">
                                <h5>
                                    Donation
                                </h5>
                            </b-nav-item>
                        </b-nav>
                    </div>
                </b-col>

            <!-- Right -->
                <b-col cols="12" md="9" class="rPart">
                    <span id="content">

                    </span>
                </b-col>
        </b-row>
    </b-container>
</template>

<script lang="ts">
  import Vue from 'vue'

  export default Vue.extend({})
</script>
