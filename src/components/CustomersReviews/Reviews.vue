<template>
    <section>
        <div class="container">

            <Head Title="review" subTitle="customers say" />
            <div class="row mt-4">
                <div class="swiper mySwiper">
                    <div class="swiper-wrapper">
                        <div class="swiper-slide text-center">
                            <img src="../../Imgs/avatar-01.jpg.webp">
                            <p class="review-text pt-5">
                                “ We are lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean tellus sem,
                                mattis in pre-<span class="d-lg-block d-inline-block">tium nec, fermentum viverra dui
                                    ”</span></p>
                            <div>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>
                            <p class="place py-3">
                                Marie Simmons ˗ New York
                            </p>
                        </div>
                        <div class="swiper-slide text-center">
                            <img src="../../Imgs/avatar-04.jpg.webp">
                            <p class="review-text pt-5">
                                “ We are lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean tellus sem,
                                mattis in pre-<span class="d-lg-block d-inline-block">tium nec, fermentum viverra dui
                                    ”</span></p>
                            <div>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>
                            <p class="place py-3">
                                Marie Simmons ˗ New York
                            </p>
                        </div>
                        <div class="swiper-slide text-center">
                            <img src="../../Imgs/avatar-05.jpg.webp">
                            <p class="review-text pt-5">
                                “ We are lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean tellus sem,
                                mattis in pre-<span class="d-lg-block d-inline-block">tium nec, fermentum viverra dui
                                    ”</span></p>
                            <div>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>
                            <p class="place py-3">
                                Marie Simmons ˗ New York
                            </p>
                        </div>
                    </div>
                    <div class="swiper-button-next"></div>
                    <div class="swiper-button-prev"></div>
                    <div class="swiper-pagination"></div>
                </div>
            </div>
        </div>
    </section>
</template>
<script scoped>
import Head from '../HeadSections/Head.vue';
import { onMounted } from 'vue';

export default {
    name: "Reviews",
    components: { Head },
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
                pagination: {
                    el: ".swiper-pagination",
                    dynamicBullets: true,
                },
            });
        })
    },
}
</script>
<style lang="scss" scoped>
@import '../../Scss/Main.scss';

section {
    background-color: white;
    padding: 100px 0px;

    img {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        border: 4px solid $Main-Color;
    }

    .review-text {
        font-size: 18px;
        color: #888787;
        font-weight: 400;
    }

    i,
    svg {
        color: $Main-Color;
    }

    .place {
        font-size: 13px;
        color: #888787;
        text-transform: uppercase;
    }
}

.swiper-button-next::after,
.swiper-button-prev::after {
    font-size: 13px !important;
    color: rgb(238, 235, 235) !important;
}

.swiper-button-next,
.swiper-button-prev {
    padding: 30px;
    background-color: rgba(0, 0, 0, 0.6);
    border-radius: 50%;
    transition: all .3s ease-in-out;
    opacity: 0;
}

.swiper-button-next:hover,
.swiper-button-prev:hover {
    background-color: rgba($Main-Color, 0.6);
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