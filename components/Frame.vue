<template>
    <b-container fluid>
        <b-row>
            <!-- Navbar -->
                <b-col cols="12" class="mNav">
                    <!-- <b-navbar toggleable="lg" type="dark" class="d-block d-lg-none d-xl-none d-md-block w-100">
                        <b-navbar-brand href="#" class="w-80">Suphakit P.</b-navbar-brand>

                        <b-navbar-toggle target="nav-collapse" class="w-20"></b-navbar-toggle>

                        <b-collapse id="nav-collapse" is-nav>
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
                    </b-navbar> -->
                    
                    <b-navbar toggleable="lg" type="dark" variant="info">
                        <b-navbar-brand href="#">NavBar</b-navbar-brand>

                        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

                        <b-collapse id="nav-collapse" is-nav>
                        <b-navbar-nav>
                            <b-nav-item href="#">Link</b-nav-item>
                            <b-nav-item href="#" disabled>Disabled</b-nav-item>
                        </b-navbar-nav>

                        <!-- Right aligned nav items -->
                        <b-navbar-nav class="ml-auto">
                            <b-nav-form>
                            <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
                            <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
                            </b-nav-form>

                            <b-nav-item-dropdown text="Lang" right>
                            <b-dropdown-item href="#">EN</b-dropdown-item>
                            <b-dropdown-item href="#">ES</b-dropdown-item>
                            <b-dropdown-item href="#">RU</b-dropdown-item>
                            <b-dropdown-item href="#">FA</b-dropdown-item>
                            </b-nav-item-dropdown>

                            <b-nav-item-dropdown right>
                            <!-- Using 'button-content' slot -->
                            <template #button-content>
                                <em>User</em>
                            </template>
                            <b-dropdown-item href="#">Profile</b-dropdown-item>
                            <b-dropdown-item href="#">Sign Out</b-dropdown-item>
                            </b-nav-item-dropdown>
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
