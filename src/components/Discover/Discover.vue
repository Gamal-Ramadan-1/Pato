<template>
    <section class="discover">
        <div class="text-center">
            <p class="text-capitalize m-0">discover</p>
            <h1 class="text-light text-uppercase fw-bold">pato place</h1>
        </div>
    </section>
</template>
<script>
export default {
    name: 'Discover'
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
</style>