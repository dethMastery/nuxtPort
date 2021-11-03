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
            <b-card no-body>
                <b-card-header v-b-toggle.blog>
                    <span>
                        Blog
                    </span>
                    <span style="float: right;">
                        <i class="fas fa-chevron-down"></i>
                    </span>
                </b-card-header>
                <b-collapse id="blog">
                    <b-card-body class="text-center">
                        <a class="s-button" href="https://blog.detzz.in.th" target="_blank">
                            <span class="logo" id="rsl">
                                <i class="fa fa-rss"></i>
                            </span>
                            <span class="text">
                                <span>
                                    blog.detzz.in.th
                                </span>
                            </span>
                        </a>
                    </b-card-body>
                </b-collapse>
            </b-card>

            <b-card no-body>
                <b-card-header v-b-toggle.facebook>
                    <span>
                        Facebook
                    </span>
                    <span style="float: right;">
                        <i class="fas fa-chevron-down"></i>
                    </span>
                </b-card-header>
                <b-collapse id="facebook">
                    <b-card-body class="text-center">
                        <a class="s-button" href="https://www.fb.com/detzz.in.th" target="_blank">
                            <span class="logo" id="fbl">
                                <i class="fab fa-facebook-f"></i>
                            </span>
                            <span class="text">
                                <span>
                                    George Deterk
                                </span>
                            </span>
                        </a>
                    </b-card-body>
                </b-collapse>
            </b-card>

            <b-card no-body>
                <b-card-header v-b-toggle.instagram>
                    <span>
                        Instagram
                    </span>
                    <span style="float: right;">
                        <i class="fas fa-chevron-down"></i>
                    </span>
                </b-card-header>
                <b-collapse id="instagram">
                    <b-card-body class="text-center">
                        <a class="s-button" href="https://www.instagram.com/detzz.th" target="_blank">
                            <span class="logo" id="igl">
                                <i class="fab fa-instagram"></i>
                            </span>
                            <span class="text">
                                <span>
                                    @detzz.th
                                </span>
                            </span>
                        </a>
                    </b-card-body>
                </b-collapse>
            </b-card>
            
            <b-card no-body>
                <b-card-header v-b-toggle.twitter>
                    <span>
                        Twitter
                    </span>
                    <span style="float: right;">
                        <i class="fas fa-chevron-down"></i>
                    </span>
                </b-card-header>
                <b-collapse id="twitter">
                    <b-card-body class="text-center">
                        <a class="s-button" href="https://twitter.com/JojiDetzz" target="_blank">
                            <span class="logo" id="twl">
                                <i class="fab fa-twitter"></i>
                            </span>
                            <span class="text">
                                <span>
                                    @JojiDetzz
                                </span>
                            </span>
                        </a>
                    </b-card-body>
                </b-collapse>
            </b-card>

            <b-card no-body>
                <b-card-header v-b-toggle.discord>
                    <span>
                        Discord
                    </span>
                    <span style="float: right;">
                        <i class="fas fa-chevron-down"></i>
                    </span>
                </b-card-header>
                <b-collapse id="discord">
                    <b-card-body class="text-center">
                        <a class="s-button" href="https://000198.xyz/w/discord" target="_blank">
                            <span class="logo" id="dcl">
                                <i class="fab fa-discord"></i>
                            </span>
                            <span class="text">
                                <span>
                                    katsuragi#0198
                                </span>
                            </span>
                        </a>
                    </b-card-body>
                </b-collapse>
            </b-card>

            <b-card no-body>
                <b-card-header v-b-toggle.github>
                    <span>
                        Github
                    </span>
                    <span style="float: right;">
                        <i class="fas fa-chevron-down"></i>
                    </span>
                </b-card-header>
                <b-collapse id="github">
                    <b-card-body class="text-center">
                        <a class="s-button" href="https://github.com/dethMastery" target="_blank">
                            <span class="logo" id="ghl">
                                <i class="fab fa-github-alt"></i>
                            </span>
                            <span class="text">
                                dethMastery
                            </span>
                        </a>
                    </b-card-body>
                </b-collapse>
            </b-card>

            <b-card no-body>
                <b-card-header v-b-toggle.email>
                    <span>
                        E-Mail
                    </span>
                    <span style="float: right;">
                        <i class="fas fa-chevron-down"></i>
                    </span>
                </b-card-header>
                <b-collapse id="email">
                    <b-card-body class="text-center">
                        <a class="s-button" href="mailto:me@detzz.in.th" target="_blank">
                            <span class="logo" id="eml">
                                <i class="fas fa-envelope"></i>
                            </span>
                            <span class="text">
                                me@detzz.in.th
                            </span>
                        </a>
                    </b-card-body>
                </b-collapse>
            </b-card>
        </div>
    </b-col>
</template>