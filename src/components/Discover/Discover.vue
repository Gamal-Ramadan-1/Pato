<template>
    <section>
        <div class="discover">
            <div class="text-center">
                <p class="text-capitalize m-0">discover</p>
                <h1 class="text-light text-uppercase fw-bold">pato place</h1>
            </div>
        </div>
        <div class="cards py-5 my-5">
            <div class="container">
                <div class="row gy-4 justify-content-center align-items-center">
                    <div class="col-lg-4 col-md-6 col-sm-12">
                        <div class="card border-0">
                            <div class="overflow-hidden card-img">
                                <img src="../../Imgs/intro-01.jpg.webp" class="card-img-top">
                            </div>
                            <div class="card-body px-0">
                                <h5 class="card-title mt-3">
                                    <a href="#"> ROMANTIC RESTAURANT</a>
                                </h5>
                                <p class="card-text py-2">Phasellus lorem enim, luctus ut velit eget, con-vallis egestas
                                    eros.</p>
                                <a href="#" class="btn text-uppercase px-0">
                                    learn more
                                    <i class="fa-solid fa-caret-right ms-2"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-4 col-md-6 col-sm-12">
                        <div class="card border-0">
                            <div class="overflow-hidden card-img">
                                <img src="../../Imgs/intro-02.jpg.webp" class="card-img-top">
                            </div>
                            <div class="card-body px-0">
                                <h5 class="card-title mt-3">
                                    <a href="#">DELICIOUS FOOD</a>
                                </h5>
                                <p class="card-text py-2">Aliquam eget aliquam magna, quis posuere risus ac justo ipsum
                                    nibh urna</p>
                                <a href="#" class="btn text-uppercase px-0">
                                    learn more
                                    <i class="fa-solid fa-caret-right ms-2"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-4 col-md-6 col-sm-12">
                        <div class="card border-0">
                            <div class="overflow-hidden card-img">
                                <img src="../../Imgs/intro-04.jpg.webp" class="card-img-top">
                            </div>
                            <div class="card-body px-0">
                                <h5 class="card-title mt-3">
                                    <a href="#">RED WINES YOU LOVE</a>
                                </h5>
                                <p class="card-text py-2">Sed ornare ligula eget tortor tempor, quis porta tellus
                                    dictum.</p>
                                <a href="#" class="btn text-uppercase px-0">
                                    learn more
                                    <i class="fa-solid fa-caret-right ms-2"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script>
export default {
    name: 'Discover',

}
</script>
<style lang="scss" scoped>
@import '../../Scss/Main.scss';

.discover {
    background-image: url('../../Imgs/bg-intro-01.jpg.webp');
    background-size: cover;
    clear: both;
    background-position: top center;
    height: 400px;
    width: 100%;
    background-attachment: fixed;
    display: flex;
    justify-content: center;
    align-items: center;

    p {
        color: $Main-Color;
        font-size: 30px;
        font-family: $Courgette-Font;
    }

    h1 {
        font-family: $Poppins-Font;
        font-size: 60px;
        letter-spacing: 10px;
    }
}

.cards {
    .card {

        .card-img {
            perspective: 600px;
            overflow: hidden;
            border-radius: 10px;

            img {
                border-radius: 10px;
                transition: all .6s ease;
                object-fit: contain;
            }

            img:hover {
                transform: translateZ(40px);
                transition: all .6s ease;
            }
        }

        h5 {
            a {
                font-weight: 500;
                letter-spacing: 3px;
                font-size: 22px;
                color: black;
                font-family: $Poppins-Font;
                text-decoration: none;
                transition: all .3s ease-in-out;
            }

            a:hover {
                color: $Main-Color;
                transition: all .3s ease-in-out;
            }
        }

        a {
            font-size: 13px;
        }

        a:hover {
            color: $Main-Color;
            transition: all .3s ease-in-out;
        }
    }
}
</style>