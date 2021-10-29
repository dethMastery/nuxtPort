<template>
    <b-col cols="12" lg="9" class="rPart" style="padding: 0!important;">
        <b-carousel
            id="carousel-1"
            indicators
            controls
            >     
            <b-carousel-slide>
                <template #img>                     
                    <div class="carousel-img img1">
                        <div class="blackscreen"></div>
                    </div>
                    <div class="carousel-caption">
                        <h5>
                            Suphakit P.
                        </h5>
                        <p>
                            1st Year Undergraduate Student / Junior Front-End Developer
                        </p>
                    </div>
                </template>
            </b-carousel-slide>

            <b-carousel-slide>
                <template #img>                     
                    <div class="carousel-img img2">
                        <div class="blackscreen"></div>
                    </div>
                    <div class="carousel-caption">
                        <h5>
                            Suphakit P.
                        </h5>
                        <p>
                            1st Year Undergraduate Student / Junior Front-End Developer
                        </p>
                    </div>
                </template>
            </b-carousel-slide>

            <b-carousel-slide>
                <template #img>                     
                    <div class="carousel-img img3">
                        <div class="blackscreen"></div>
                    </div>
                    <div class="carousel-caption">
                        <h5>
                            Suphakit P.
                        </h5>
                        <p>
                            1st Year Undergraduate Student / Junior Front-End Developer
                        </p>
                    </div>
                </template>
            </b-carousel-slide>
        </b-carousel>
    </b-col>
</template>

<style>
    .img1 {
        background-image: url('https://box.lolis.love/0/hflzv.webp');
        width: 100%;
        height: 100%;
        background-size: cover;
        background-position: center;
    }

    .img2 {
        background-image: url('https://box.lolis.love/0/et7et.webp');
        width: 100%;
        height: 100%;
        background-size: cover;
        background-position: center;
    }

    .img3 {
        background-image: url('https://box.lolis.love/0/d82jx.webp');
        width: 100%;
        height: 100%;
        background-size: cover;
        background-position: center;
    }
</style>