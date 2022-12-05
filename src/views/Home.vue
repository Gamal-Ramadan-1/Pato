<template>
    <SliderHome />
    <Welcome />
    <Discover />
</template>
<script>
import Discover from '../components/Discover/Discover.vue';
import SliderHome from '../components/Sliders/Slider-Home.vue';
import Welcome from '../components/Welcome/Welcome.vue';

export default {
    name: "Menu",
    components: { SliderHome, Welcome, Discover }
}
</script>
<style lang="scss" scoped>
@import '../Scss/Main.scss';
</style>