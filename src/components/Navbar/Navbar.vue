<template>
    <Transition>
        <section class="nav-1" v-show="(scY < 1)">
            <div class="line p-1 m-0"></div>
            <div class="container">
                <div class="row p-3 justify-content-center align-items-center">
                    <div class="col p-0">
                        <a href="#">
                            <img src="@/Imgs/logo.png.webp">
                        </a>
                    </div>
                    <div class="col d-lg-inline-block d-none p-0">
                        <ul class="m-0 p-0">
                            <li class="text-uppercase">
                                <RouterLink to="/" tag="a" class="p-0 ms-4">Home</RouterLink>
                            </li>
                            <li class="text-uppercase">
                                <RouterLink to="/menu" tag="a" class="p-0 ms-4">menu</RouterLink>
                            </li>
                            <li class="text-uppercase">
                                <RouterLink to="/reservation" tag="a" class="p-0 ms-4">reservation</RouterLink>
                            </li>
                            <li class="text-uppercase">
                                <RouterLink to="/gallary" tag="a" class="p-0 ms-4">gallary</RouterLink>
                            </li>
                            <li class="text-uppercase">
                                <RouterLink to="/about" tag="a" class="p-0 ms-4">about</RouterLink>
                            </li>
                            <li class="text-uppercase">
                                <RouterLink to="/blog" tag="a" class="p-0 ms-4">blog</RouterLink>
                            </li>
                            <li class="text-uppercase">
                                <RouterLink to="/contact" tag="a" class="p-0 ms-4">contact</RouterLink>
                            </li>
                        </ul>
                    </div>
                    <div class="col p-0">
                        <div class="icons float-end">
                            <p class="d-inline-block m-0">
                                <i class="fa-brands fa-youtube mx-2"></i>
                            </p>
                            <p class="d-inline-block m-0">
                                <i class="fa-brands fa-facebook-f mx-2"></i>
                            </p>
                            <p class="d-inline-block m-0">
                                <i class="fa-brands fa-twitter mx-2"></i>
                            </p>
                            <p @click="showSlideNav()" class="d-inline-block m-0">
                                <i class="fa-solid fa-bars mx-2"></i>
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </Transition>
    <Transition>

        <section class="nav-2" v-show="(scY > 1)">
            <div class="line p-1 m-0"></div>
            <div class="container">
                <div class="row p-3 justify-content-center align-items-center">
                    <div class="col p-0">
                        <a href="#">
                            <img src="../../Imgs/logo2.png.webp">
                        </a>
                    </div>
                    <div class="col d-lg-inline-block d-none p-0">
                        <ul class="m-0 p-0">
                            <li class="text-uppercase">
                                <RouterLink to="/" tag="a" class="p-0 ms-4">Home</RouterLink>
                            </li>
                            <li class="text-uppercase">
                                <RouterLink to="/menu" tag="a" class="p-0 ms-4">menu</RouterLink>
                            </li>
                            <li class="text-uppercase">
                                <RouterLink to="/reservation" tag="a" class="p-0 ms-4">reservation</RouterLink>
                            </li>
                            <li class="text-uppercase">
                                <RouterLink to="/gallary" tag="a" class="p-0 ms-4">gallary</RouterLink>
                            </li>
                            <li class="text-uppercase">
                                <RouterLink to="/about" tag="a" class="p-0 ms-4">about</RouterLink>
                            </li>
                            <li class="text-uppercase">
                                <RouterLink to="/blog" tag="a" class="p-0 ms-4">blog</RouterLink>
                            </li>
                            <li class="text-uppercase">
                                <RouterLink to="/contact" tag="a" class="p-0 ms-4">contact</RouterLink>
                            </li>
                        </ul>
                    </div>
                    <div class="col p-0">
                        <div class="icons float-end">
                            <p class="d-inline-block m-0">
                                <i class="fa-brands fa-youtube mx-2"></i>
                            </p>
                            <p class="d-inline-block m-0">
                                <i class="fa-brands fa-facebook-f mx-2"></i>
                            </p>
                            <p class="d-inline-block m-0">
                                <i class="fa-brands fa-twitter mx-2"></i>
                            </p>
                            <p @click="showSlideNav()" class="d-inline-block m-0">
                                <i class="fa-solid fa-bars mx-2"></i>
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </Transition>
    <SideNavmenu class="sideNav m-0" />
    <RouterView />
</template>
<script>
import SideNavmenu from '../SideNavmenu/SideNavmenu.vue';
export default {
    name: "Navbar",
    components: { SideNavmenu },
    data() {
        return {
            scY: 0
        }
    },
    mounted() {
        window.addEventListener('scroll', this.handelescroll)
    },
    methods: {
        handelescroll: function () {
            this.scY = window.scrollY
        },
        showSlideNav() {
            $('.sideNav').css({ "display": "block" })
        }
    }
}
$(document).ready(function () {
    $('.sideNav').css('display', 'none')
    if (this.scY <= 100) {
        $('.sideNav').css('display', 'none')
    }
})
</script>
<style lang="scss" scoped>
@import '@/Scss/Main.scss';

.nav-1 {
    position: absolute;
    font-family: Montserrat;
    background: linear-gradient(rgba(0, 0, 0, 0.6), transparent);
    z-index: 1;
    width: 100%;

    .line {
        background-color: $Main-Color;
        width: 100%;
    }

    ul {
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 0px;

        li {
            list-style: none;
            float: left;

            a {
                color: white !important;
                text-decoration: none !important;
                font-weight: 200;
                transition: all .3s ease-in-out;
            }

            a:hover {
                color: $Main-Color !important;
                transition: all .3s ease-in-out;
            }
        }
    }


    .icons {

        i,
        svg {
            color: white;
            transition: all .3s ease-in-out;
            cursor: pointer;
        }

        i:hover,
        svg:hover {
            color: $Main-Color;
            transition: all .3s ease-in-out;
        }
    }

}

@media only screen and (max-width:768px) {
    ul {
        display: none !important;
    }
}


.nav-2 {
    font-family: Montserrat;
    background: rgba(255, 255, 255, 0.7);
    backdrop-filter: blur(2px);
    position: fixed;
    z-index: 998;
    width: 100%;
    box-shadow: 0px 0px 5px gray;

    ul {
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 0px;

        li {
            list-style: none;
            float: left;

            a {
                color: black !important;
                text-decoration: none !important;
                font-weight: 200;
                transition: all .3s ease-in-out;
            }

            a:hover {
                color: $Main-Color !important;
                transition: all .3s ease-in-out;
            }
        }
    }


    .line {
        background-color: $Main-Color;
    }

    .icons {

        i,
        svg {
            transition: all .3s ease-in-out;
            cursor: pointer;
        }

        i:hover,
        svg:hover {
            color: $Main-Color;
            transition: all .3s ease-in-out;
        }
    }
}

.v-enter-active,
.v-leave-active {
    transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
    opacity: 0;
}
</style>