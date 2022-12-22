<template>
    <section class="swiper mySwiper">
        <div class="swiper-wrapper h-100">
            <div class="swiper-slide h-100 peppar-1">

                <Head Title="events" subTitle="upcomming" titleColor="text-light" class="pt-5 pb-3 mt-5" />
                <div class="container">
                    <div class="row">
                        <div class="col-lg-6 p-0">
                            <div class="content-left-part w-100">
                                <img src="../../Imgs/event-02.jpg.webp" class="img-fluid">
                                <div class="time-event p-3">
                                    <p class="text-light m-0">08:00 pm tuesday - 21 novamber 2022</p>
                                </div>
                            </div>
                        </div>
                        <div class="col-lg-6 p-0">
                            <div class="text-center bg-light p-5">
                                <h4 class="text-uppercase fw-bold">wines during specific nights</h4>
                                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit veritatis beatae
                                    recusandae itaque sed</p>
                                <Time />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="swiper-slide h-100 peppar-2">

                <Head Title="events" subTitle="upcomming" titleColor="text-light" class="pt-5 pb-3 mt-5" />
                <div class="container">
                    <div class="row">
                        <div class="col-lg-6 p-0">
                            <div class="content-left-part w-100">
                                <img src="../../Imgs/event-01.jpg.webp" class="img-fluid">
                                <div class="time-event p-3">
                                    <p class="text-light m-0">08:00 pm tuesday - 21 novamber 2022</p>
                                </div>
                            </div>
                        </div>
                        <div class="col-lg-6 p-0">
                            <div class="text-center bg-light p-5">
                                <h4 class="text-uppercase fw-bold">wines during specific nights</h4>
                                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit veritatis beatae
                                    recusandae itaque sed</p>
                                <Time />

                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="swiper-slide h-100 peppar-3">

                <Head Title="events" subTitle="upcomming" titleColor="text-light" class="pt-5 pb-3 mt-5" />
                <div class="container">
                    <div class="row">
                        <div class="col-lg-6 p-0">
                            <div class="content-left-part w-100">
                                <img src="../../Imgs/event-06.jpg.webp" class="img-fluid">
                                <div class="time-event p-3">
                                    <p class="text-light m-0">08:00 pm tuesday - 21 novamber 2022</p>
                                </div>
                            </div>
                        </div>
                        <div class="col-lg-6 p-0">
                            <div class="text-center bg-light p-5 border-rounded-end">
                                <h4 class="text-uppercase fw-bold">wines during specific nights</h4>
                                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit veritatis beatae
                                    recusandae itaque sed</p>
                                <!-- <Time /> -->
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="swiper-button-next me-lg-3 m-0"></div>
        <div class="swiper-button-prev ms-lg-3 m-0"></div>

    </section>
</template>
<script>
import Head from '../HeadSections/Head.vue';
import { onMounted } from 'vue';
import Time from '../TimeOffer/Time.vue';
export default {
    name: "Events",
    components: { Head, Time },
    setup() {
        onMounted(() => {
            let swiper = new Swiper(".mySwiper", {
                slidesPerGroup: 1,
                autoplay: true,
                speed: 1000,
                loop: true,
                effect: "fade",
                navigation: {
                    nextEl: ".swiper-button-next",
                    prevEl: ".swiper-button-prev",
                },
            });
        })
    },
}
</script>
<style lang="scss" scoped>
@import '../../Scss/Main.scss';

section {
    height: 120vh;
    position: relative;
    z-index: 0;
    width: 100%;

    .peppar-1,
    .peppar-2,
    .peppar-3 {
        background-size: cover;
        background-position: center center;
        background-repeat: no-repeat;
        clear: both;
    }

    .peppar-1 {
        background-image: url('../../Imgs/bg-event-01.jpg.webp');
    }

    .peppar-2 {
        background-image: url('../../Imgs/bg-event-02.jpg.webp');
    }

    .peppar-3 {
        background-image: url('../../Imgs/bg-event-04.jpg.webp');
    }

    .content-left-part {
        position: relative;
        overflow: hidden;
        border-radius: 20px 0px 0px 20px;

        .time-event {
            position: absolute;
            z-index: 1;
            top: 170px;
            left: -305px;
            background-color: rgba($Main-Color, .8);
            transform: rotate(-270deg);
            width: 100%;
            text-align: center;
            font-size: 14px;
            text-transform: uppercase;
        }
    }
}

.swiper-button-next::after,
.swiper-button-prev::after {
    font-size: 15px !important;
    color: rgb(203, 202, 202) !important;
}

.swiper-button-next,
.swiper-button-prev {
    padding: 35px;
    background-color: rgba(0, 0, 0, 0.4);
    border-radius: 50%;
    transition: all .3s ease-in-out;
    opacity: 0;
}

.swiper-button-next:hover,
.swiper-button-prev:hover {
    background-color: rgba(255, 0, 0, 0.3);
    transition: all .3s ease-in-out;
}

.swiper:hover {

    .swiper-button-next,
    .swiper-button-prev {
        opacity: 1;
        transition: all .3s ease-in-out;
    }
}
</style>