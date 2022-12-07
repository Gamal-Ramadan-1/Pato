<template>
    <section class="our-blog py-5">
        <div class="container my-5">

            <Head Title="our menu" subTitle="Discover" />
            <div class="row gy-4 mt-4">
                <div class="col-lg-4 col-md-4">
                    <div class="content position-relative">
                        <img src="../../Imgs/our-menu-01.jpg.webp" class="img-fluid">
                        <div class="btn position-absolute px-5 py-3">lunch</div>
                    </div>
                </div>
                <div class="col-lg-4 col-md-4">
                    <div class="content position-relative">
                        <img src="../../Imgs/our-menu-05.jpg.webp" class="img-fluid">
                        <div class="btn position-absolute px-5 py-3">dinner</div>
                    </div>
                </div>
                <div class="col-lg-4 col-md-4">
                    <div class="row gy-3">
                        <div class="col-12">
                            <div class="content position-relative">
                                <img src="../../Imgs/our-menu-08.jpg.webp" class="img-fluid">
                                <div class="btn position-absolute px-5 py-3">drink</div>
                            </div>
                        </div>
                        <div class="col-12 pt-3">
                            <div class="content position-relative starters">
                                <img src="../../Imgs/our-menu-10.jpg.webp" class="img-fluid">
                                <div class="btn position-absolute px-5 py-3">STARTERS</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row my-4 gy-4">
                <div class="col-lg-8 col-md-8">
                    <div class="content position-relative happy-hour">
                        <img src="../../Imgs/our-menu-13.jpg.webp" class="happy-hour-img">
                        <div class="btn position-absolute px-5 py-3">happy hour</div>
                    </div>
                </div>
                <div class="col-lg-4 col-md-4">
                    <div class="content position-relative">
                        <img src="../../Imgs/our-menu-16.jpg.webp" class="img-fluid">
                        <div class="btn position-absolute px-5 py-3">dessert</div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script>
import Head from '../HeadSections/Head.vue';

export default {
    name: 'OurMenu',
    components: { Head }
}
</script>
<style lang="scss" scoped>
@import '../../Scss/Main.scss';

section {
    background-color: #F5F2EC;

    .content {
        border-radius: 20px;
        perspective: 600px;
        overflow: hidden;

        img {
            border-radius: 10px;
            transition: all .4s ease;
        }

        .btn {
            z-index: 1;
            top: 45%;
            left: 30%;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: rgba(255, 255, 255, .9);
            border-radius: 10px;
            color: black;
            text-transform: uppercase;
            font-weight: bold;
            font-size: 20px;
            transition: all .4s ease;
        }

        .btn:hover {
            background-color: rgba($color: $Main-Color, $alpha: .8);
            color: white;
            transition: all .4s ease;
        }
    }
}

.content:hover {
    img {
        transform: translateZ(40px);
        transition: all .4s ease;
    }
}

.happy-hour {

    .happy-hour-img {
        width: 100%;
    }

    .btn {
        top: 40% !important;
        left: 35% !important;
    }
}



@media only screen and (max-width:1024px) {
    .btn {
        top: 35% !important;
        left: 20% !important;
    }

    .happy-hour {

        .happy-hour-img {
            width: 100%;
        }

        .btn {
            top: 32% !important;
            left: 30% !important;
        }
    }
}

@media only screen and (max-width:768px) {
    .starters {
        .btn {
            top: 25% !important;
            left: 4% !important;
        }
    }

    .btn {
        top: 32% !important;
        left: 8% !important;
    }

    .happy-hour {

        .happy-hour-img {
            width: 100%;
        }

        .btn {
            top: 27% !important;
            left: 25% !important;
        }
    }

}

@media only screen and (max-width:426px) {
    .btn {
        top: 40% !important;
        left: 27% !important;
    }

    .happy-hour {

        .happy-hour-img {
            width: 100%;
        }

        .btn {
            top: 25% !important;
            left: 20% !important;
        }
    }

    .starters {
    .btn {
        top: 35% !important;
        left: 25% !important;
    }
}
}

@media only screen and (max-width:375px) {
    .btn {
        top: 30% !important;
        left: 15% !important;
    }

    .happy-hour {

        .happy-hour-img {
            width: 100%;
        }

        .btn {
            top: 25% !important;
            left: 21% !important;
        }
    }
}

@media only screen and (max-width:320px) {
    .btn {
        top: 35% !important;
        left: 21% !important;
    }

    .happy-hour {

        .happy-hour-img {
            width: 100%;
        }

        .btn {
            top: 15% !important;
            left: 11% !important;
        }
    }

    .starters {
        .btn {
            top: 35% !important;
            left: 17% !important;
        }
    }
}
</style>