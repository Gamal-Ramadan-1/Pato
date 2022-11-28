<template>
    <section class="welcome">
        <div class="container">
            <div class="row gy-5">
                <div class="col-lg-6 col-sm-12 text-center pt-5 px-3">
                    <div class="head">
                        <p>Italian Restaurant</p>
                        <h1 class="text-uppercase">welcome</h1>
                    </div>
                    <p class="mx-md-4">Donec quis lorem nulla. Nunc eu odio mi. Morbi nec lobortis est. Sed fringilla,
                        nunc sed
                        imperdiet lacinia, nisl ante egestas mi, ac facilisis ligula sem id neque.

                    </p>
                    <a href="#" class="btn text-uppercase p-0">our store
                        <i class="fa-solid fa-caret-right ms-1"></i>
                    </a>
                </div>
                <div class="col-lg-6 col-sm-12 d-flex justify-content-center align-items-center">
                    <div class="content-img">
                        <img src="../../Imgs/our-story-01.jpg.webp" class="img-fluid">
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script>
export default {
    name: 'Welcome'
}
</script>
<style lang="scss" scoped>
@import '@/Scss/Main.scss';

.welcome {
    background-image: url('../../Imgs/pattern1.png.webp');
    background-size: cover;
    clear: both;
    background-position: 50% 50%;
    padding: 120px 0px;

    .head {
        p {
            color: $Main-Color;
            font-family: $Courgette-Font;
            font-size: 30px;
            padding: 0px;
            margin: 0px;
        }

        h1 {
            font-family: $Poppins-Font;
            letter-spacing: 8px;
            margin-bottom: 30px;
            font-weight: 700;
            font-size: 50px;
        }
    }

    p {
        color: #666666
    }

    .btn {
        font-size: 13px;
        color: #666666;
        transition: all .3s ease-in-out;

        i,
        svg {
            transition: all .3s ease-in-out;
        }
    }

    .btn:hover {
        color: $Main-Color;
        transition: all .3s ease-in-out;

        i,
        svg {
            transform: translate(8px, 0px);
            transition: all .3s ease-in-out;
            color: $Main-Color;
        }
    }

    .content-img {
        overflow: hidden;
        perspective: 600px;
        width: 60%;
        border-radius: 10px;

        img {
            height: auto;
            object-fit: cover;
            border-radius: 10px;
            transition: all .4s ease-in;
        }

        img:hover {
            transition: all .4s ease-in;
            transform: translateZ(40px);
        }
    }
}

@media only screen and (max-width:426px) {
    .content-img {
        width: 100% !important;
    }
}
</style>