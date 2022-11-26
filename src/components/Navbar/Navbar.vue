<template>
    <section class="test">
        <div class="line p-1 m-0"></div>
        <nav class="navbar navbar-expand-lg">
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
                <div class="icons float-start">
                    <p class="d-inline-block m-0">
                        <i class="fa-brands fa-facebook-f mx-3"></i>
                    </p>
                    <p class="d-inline-block m-0">
                        <i class="fa-brands fa-twitter mx-3"></i>
                    </p>
                    <p @click="showSlideNav()" class="d-inline-block m-0">
                        <i class="fa-solid fa-bars mx-3"></i>
                    </p>
                </div>
            </div>
        </nav>
    </section>
    <SideNavmenu class="sideNav" />
    <RouterView />
</template>
<script>
import SideNavmenu from '../SideNavmenu/SideNavmenu.vue';
$(document).ready(function () {
    $('.sideNav').css('display', 'none')
})
export default {
    name: "Navbar",
    components: { SideNavmenu },

    methods: {

        showSlideNav() {
            $('.sideNav').css({ "display": "inline-block" })
        }
    }
}
</script>
<style lang="scss" scoped>
@import '@/Scss/Main.scss';

section {
    font-family: Montserrat;

    .line {
        background-color: $Main-Color;
        width: 100%;
    }

    .nav-link {
        color: white;
        font-weight: 200;
    }

    .nav-link:hover {
        color: $Main-Color;
    }

    .icons {

        i,
        svg {
            color: white;
            cursor: pointer;
        }
    }

}

@media only screen and (max-width:768px) {
    .navbar-nav {
        display: none;
    }
}
</style>