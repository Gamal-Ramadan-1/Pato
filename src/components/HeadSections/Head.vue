<template>
    <div class="row py-3">
        <div class="col-12 text-center">
            <p class="text-capitalize">{{ subTitle }}</p>
            <h1 :class="titleColor + ' text-uppercase'">{{ Title }}</h1>
        </div>
    </div>
</template>
<script>
export default {
    name: 'Head',
    props: { subTitle: String, Title: String, titleColor: String }
}
</script>
<style lang="scss" scoped>
@import '../../Scss/Main.scss';

p {
    font-size: 30px;
    font-family: $Courgette-Font;
    color: $Main-Color;
    line-height: 1.2;
}

h1 {
    font-family: $Poppins-Font;
    font-weight: 700;
    font-size: 50px;
    line-height: 1.2;
    letter-spacing: 10px;
    word-spacing: 8px;
}
</style>