<template>
    <SliderHome />
    <Welcome />
    <Discover />
    <OurMenu />
</template>
<script>
import Discover from '../components/Discover/Discover.vue';
import OurMenu from '../components/OurMenu-Section-In-Home/OurMenu.vue';
import SliderHome from '../components/Sliders/Slider-Home.vue';
import Welcome from '../components/Welcome/Welcome.vue';

export default {
    name: "Menu",
    components: { SliderHome, Welcome, Discover, OurMenu }
}
</script>
<style lang="scss" scoped>
@import '../Scss/Main.scss';
</style>