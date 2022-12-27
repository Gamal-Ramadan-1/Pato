<template>
    <SliderHome />
    <Welcome />
    <Discover />
    <OurMenu />
    <Events />
    <BookTable />
    <Reviews />
    <OurVideo />
</template>
<script>
import BookTable from '../components/BookingTable/BookTable.vue';
import Reviews from '../components/CustomersReviews/Reviews.vue';
import Discover from '../components/Discover/Discover.vue';
import Events from '../components/Events-section/Events.vue';
import OurMenu from '../components/OurMenu-Section-In-Home/OurMenu.vue';
import OurVideo from '../components/OurVideo/OurVideo.vue';
import SliderHome from '../components/Sliders/Slider-Home.vue';
import Welcome from '../components/Welcome/Welcome.vue';

export default {
    name: "Menu",
    components: { SliderHome, Welcome, Discover, OurMenu, Events, BookTable, Reviews, OurVideo }
}
</script>
<style lang="scss" scoped>
@import '../Scss/Main.scss';
</style>