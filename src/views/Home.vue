<template>
    <SliderHome />
    <Welcome />
</template>
<script>
import SliderHome from '../components/Sliders/Slider-Home.vue';
import Welcome from '../components/Welcome/Welcome.vue';

export default {
    name: "Menu",
    components: { SliderHome, Welcome }
}
</script>
<style lang="scss" scoped>
@import '../Scss/Main.scss';
</style>