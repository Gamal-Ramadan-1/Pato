<template>
    <section class="nav-1" v-show="scY < 250">
        <div class="line p-1 m-0"></div>
        <nav class="navbar navbar-expand-lg py-3">
            <div class="container">
                <a class="navbar-brand" href="#">
                    <img src="@/Imgs/logo.png.webp">
                </a>
                <ul class="navbar-nav">
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/" tag="a" class="nav-link p-0 m-2">Home</RouterLink>
                    </li>
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/menu" tag="a" class="nav-link p-0 m-2">menu</RouterLink>
                    </li>
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/reservation" tag="a" class="nav-link p-0 m-2">reservation</RouterLink>
                    </li>
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/gallary" tag="a" class="nav-link p-0 m-2">gallary</RouterLink>
                    </li>
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/about" tag="a" class="nav-link p-0 m-2">about</RouterLink>
                    </li>
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/blog" tag="a" class="nav-link p-0 m-2">blog</RouterLink>
                    </li>
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/contact" tag="a" class="nav-link p-0 m-2">contact</RouterLink>
                    </li>
                </ul>
                <div class="icons float-start d-flex justify-content-center align-items-center">
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
        </nav>
    </section>
    <section class="nav-2" v-show="scY > 340">
        <div class="line p-1 m-0"></div>
        <nav class="navbar navbar-expand-lg py-3">
            <div class="container">
                <a class="navbar-brand" href="#">
                    <img src="@/Imgs/logo2.png.webp">
                </a>
                <ul class="navbar-nav">
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/" tag="a" class="nav-link p-0 m-2">Home</RouterLink>
                    </li>
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/menu" tag="a" class="nav-link p-0 m-2">menu</RouterLink>
                    </li>
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/reservation" tag="a" class="nav-link p-0 m-2">reservation</RouterLink>
                    </li>
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/gallary" tag="a" class="nav-link p-0 m-2">gallary</RouterLink>
                    </li>
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/about" tag="a" class="nav-link p-0 m-2">about</RouterLink>
                    </li>
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/blog" tag="a" class="nav-link p-0 m-2">blog</RouterLink>
                    </li>
                    <li class="nav-item text-uppercase px-4">
                        <RouterLink to="/contact" tag="a" class="nav-link p-0 m-2">contact</RouterLink>
                    </li>
                </ul>
                <div class="icons float-start d-flex justify-content-center align-items-center">
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
        </nav>
    </section>
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

    .nav-link {
        color: white;
        font-weight: 200;
        transition: all .3s ease-in-out;
    }

    .nav-link:hover {
        color: $Main-Color;
        transition: all .3s ease-in-out;

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
    .navbar-nav {
        display: none;
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

    .nav-link {
        color: black;
        transition: all .3s ease-in-out;

    }

    .nav-link:hover {
        color: $Main-Color;
        transition: all .3s ease-in-out;
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
</style>