<template>
    <section class="hide">
        <div class="side-nav-menu ">
            <div class="position-relative w-100">
                <a class="close float-end" @click="close()">&times;</a>
            </div>
            <ul class="navbar-nav w-100 text-center pt-5">
                <li class="nav-item text-uppercase px-4">
                    <p class="d-inline-block m-0">
                        <RouterLink to="/" tag="a" class="nav-link p-0 my-1" @click="close()">Home</RouterLink>
                    </p>
                </li>
                <li class="nav-item text-uppercase px-4">
                    <p class="d-inline-block m-0">
                        <RouterLink to="/menu" tag="a" class="nav-link p-0 my-2" @click="close()">menu</RouterLink>
                    </p>
                </li>
                <li class="nav-item text-uppercase px-4">
                    <p class="d-inline-block m-0">
                        <RouterLink to="/gallary" tag="a" class="nav-link p-0 my-2" @click="close()">gallary
                        </RouterLink>
                    </p>
                </li>
                <li class="nav-item text-uppercase px-4">
                    <p class="d-inline-block m-0">
                        <RouterLink to="/about" tag="a" class="nav-link p-0 my-2" @click="close()">about</RouterLink>
                    </p>
                </li>
                <li class="nav-item text-uppercase px-4">
                    <p class="d-inline-block m-0">
                        <RouterLink to="/blog" tag="a" class="nav-link p-0 my-2" @click="close()">blog</RouterLink>
                    </p>
                </li>
                <li class="nav-item text-uppercase px-4">
                    <p class="d-inline-block m-0">
                        <RouterLink to="/contact" tag="a" class="nav-link p-0 my-2" @click="close()">contact
                        </RouterLink>
                    </p>
                </li>
                <div class="btn align-self-center text-uppercase px-4 mt-4 py-1">
                    <RouterLink to="/reservation" tag="a" class="nav-link p-0 my-2" @click="close()">reservation
                    </RouterLink>
                </div>
            </ul>
            <div class="gallary container pt-5 mt-5 mb-3">
                <div class="row">
                    <h5 class="text-uppercase text-center">gallary</h5>
                </div>
                <div class="row g-2 px-3 mt-4">
                    <div class="col-4">
                        <div class="img-gallary">
                            <img src="../../Imgs/photo-gallery-thumb-01.jpg.webp" class="img-fluid">
                            <div class="layout-img"></div>
                        </div>
                    </div>
                    <div class="col-4">
                        <div class="img-gallary">
                            <img src="../../Imgs/photo-gallery-thumb-02.jpg.webp" class="img-fluid">
                            <div class="layout-img"></div>
                        </div>
                    </div>
                    <div class="col-4">
                        <div class="img-gallary">
                            <img src="../../Imgs/photo-gallery-thumb-03.jpg.webp" class="img-fluid">
                            <div class="layout-img"></div>
                        </div>
                    </div>
                    <div class="col-4">
                        <div class="img-gallary">
                            <img src="../../Imgs/photo-gallery-thumb-04.jpg.webp" class="img-fluid">
                            <div class="layout-img"></div>
                        </div>
                    </div>
                    <div class="col-4">
                        <div class="img-gallary">
                            <img src="../../Imgs/photo-gallery-thumb-05.jpg.webp" class="img-fluid">
                            <div class="layout-img"></div>
                        </div>
                    </div>
                    <div class="col-4">
                        <div class="img-gallary">
                            <img src="../../Imgs/photo-gallery-thumb-06.jpg.webp" class="img-fluid">
                            <div class="layout-img"></div>
                        </div>
                    </div>
                    <div class="col-4">
                        <div class="img-gallary">
                            <img src="../../Imgs/photo-gallery-thumb-07.jpg.webp" class="img-fluid">
                            <div class="layout-img"></div>
                        </div>
                    </div>
                    <div class="col-4">
                        <div class="img-gallary">
                            <img src="../../Imgs/photo-gallery-thumb-08.jpg.webp" class="img-fluid">
                            <div class="layout-img"></div>
                        </div>
                    </div>
                    <div class="col-4">
                        <div class="img-gallary">
                            <img src="../../Imgs/photo-gallery-thumb-09.jpg.webp" class="img-fluid">
                            <div class="layout-img"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="layout" @click="close()"></div>
    </section>
</template>
<script>
export default {
    name: 'SideNavmenu',
    methods: {
        close() {
            $('.hide').css({ 'display': 'none' })
        }
    }
}
</script>
<style lang="scss" scoped>
@import '../../Scss/Main.scss';

a {
    text-decoration: none;
}

.hide {
    .close {
        color: black;
        font-size: 45px;
        font-weight: lighter;
        right: 20px;
        top: 10px;
        cursor: pointer;
    }

    .close:hover {
        color: $Main-Color !important;
    }


    .side-nav-menu {
        background-color: white;
        width: 300px;
        position: fixed;
        height: 100vh;
        overflow: auto;
        z-index: 1000;
        top: 0px;
        right: 0px;

        .btn {
            background-color: $Copyright-Color;
            color: white;
            transition: all .3s ease-in-out;
            font-size: 15px;

            a:hover {
                color: white !important;
            }
        }

        .btn:hover {
            background-color: $Main-Color;
            transition: all .3s ease-in-out;
            color: white !important;
        }


    }

    .nav-link:hover {
        color: $Main-Color !important;
    }

    .layout {
        width: 100%;
        height: 100%;
        background-color: $Copyright-Color;
        position: fixed;
        z-index: 999;
        top: 0px;
        opacity: .5;
        cursor: pointer;
    }
}

.img-gallary {
    position: relative;

    .layout-img {
        position: absolute;
        width: 100%;
        height: 100%;
        background-color: $Main-Color;
        z-index: 2;
        opacity: 0;
        top: 0px;
        transition: all .4s ease-in-out
    }
}

.img-gallary:hover {
    .layout-img {
        opacity: .7;
        top: 0px;
        left: 0px;
        transition: all .4s ease-in-out;
        cursor: pointer;
    }
}
</style>