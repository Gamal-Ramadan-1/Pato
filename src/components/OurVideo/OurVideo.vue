<template>
    <section class="position-reletive">
        <div class="layout-2">
            <div style="height: 10%;">
                <h1 @click="closeVideo()" class="close">&times;</h1>
            </div>
            <div style="display: flex; justify-content: center; align-items: center; height: 90%;">
                <video width="400" height="300" controls> 
                    <source src="../../Videos/b8430f578a00c75704b858b7a1ba0454.mp4.mp4">
                    <source src="../../Videos/5477c63df0c175413a9c93763700b287.mp4.mp4">
                    Your Browser Dosn't Support Our Video
                </video>
            </div>
        </div>
        <div class="container">
            <header>

                <Head Title="our video" subTitle="Discover" titleColor="text-light" />
            </header>
            <main>
                <div class="row">
                    <div class="col-12 text-center d-flex justify-content-center" style="perspective: 600px;">
                        <div class="btn" @click="openVideo()">
                            <i class="fa-solid fa-play"></i>
                        </div>
                    </div>
                </div>
            </main>
        </div>
    </section>
</template>
<script scoped>
import Head from '../HeadSections/Head.vue';

export default {
    name: "OurVideo",
    components: { Head },
    methods: {
        closeVideo() {
            $('.layout-2').css({ 'display': 'none' })
            $('video').css({ 'display': 'none' })
        },
        openVideo() {
            $('.layout-2').css({ 'display': 'inline-block' })
            $('video').css({ 'display': 'inline-block' })
        }
    }
}
</script>
<style lang="scss" scoped>
@import '../../Scss/Main.scss';

a {
    text-decoration: none;
}

section {
    width: 100%;
    padding: 250px 0px;
    background-image: url('../../Imgs/bg-cover-video-02.jpg.webp');
    background-position: center - 15.05px;
    background-attachment: fixed;
    clear: both;
    background-size: cover;

    .btn {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 65px;
        height: 65px;
        border-radius: 50%;
        background-color: white;
        font-size: 15px;
        color: black;
        transition: all .4s ease;

    }

    .btn:hover {
        transform: translateZ(100px);
        background-color: rgba($color: $Main-Color, $alpha: .7);
        color: white;
        transition: all .4s ease;
    }
}

.layout-2 {
    position: fixed;
    top: 0px;
    width: 100%;
    height: 100vh;
    background-color: rgba(black, 0.8);
    z-index: 2000;
    display: none;

    .close {
        position: absolute;
        top: 0px;
        cursor: pointer;
        right: 20px;
        font-size: 50px;
        color: #AAA;
    }
}
</style>