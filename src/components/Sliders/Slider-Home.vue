<template>
  <div class="swiper mySwiper">
    <div class="swiper-wrapper h-100">
      <div class="swiper-slide h-100 main-pepper">
        <div class="text-center">
          <h3 class="text-light w-100 text-center animsition" data-animsition-in-class="fade-in-left-lg"
            data-animsition-out-Duration="1500">Wellcome to
          </h3>
          <h1 class="text-light w-100 text-center text-uppercase animsition" data-animsition-in-class="fade-in-right-lg"
            data-animsition-out-Duration="2000">
            pato place</h1>
          <div class="btn text-center text-capitalize px-4 mt-4 animsition" data-animsition-in-class="rotate-in-lg"
            data-animsition-out-Duration="2000">look
            menu</div>
        </div>
      </div>
      <div class="swiper-slide h-100 pepper-2">
        <div class="text-center">
          <h3 class="text-light w-100 text-center">Wellcome to</h3>
          <h1 class="text-light w-100 text-center text-uppercase">pato place</h1>
          <div class="btn text-center text-capitalize px-4 mt-4">look menu</div>
        </div>
      </div>
      <div class="swiper-slide h-100 pepper-3">
        <div class="text-center">
          <h3 class="text-light w-100 text-center">Wellcome to</h3>
          <h1 class="text-light w-100 text-center text-uppercase">pato place</h1>
          <div class="btn text-center text-capitalize px-4 mt-4">look menu</div>
        </div>
      </div>
    </div>
    <div class="swiper-button-next me-lg-3 m-0"></div>
    <div class="swiper-button-prev ms-lg-3 m-0"></div>
  </div>
</template>
<script>
import { onMounted } from 'vue';
export default {
  name: 'SliderHome',
  setup() {
    onMounted(() => {
      let swiper = new Swiper(".mySwiper", {
        slidesPerGroup: 1,
        autoplay: true,
        speed: 1000,
        loop: true,
        effect: "fade",
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
      });
      $('.animsition').animsition({
        loading: false,
      })
    });
  },
}
</script>

<style lang="scss" scoped>
@import '../../Scss/Main.scss';

.swiper {
  position: relative;
  z-index: 0;
  height: 100vh;
  width: 100%;

  .swiper-slide {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
  }

  .main-pepper,
  .pepper-2,
  .pepper-3 {
    background-size: cover;
    background-position: 50% 50%;
    background-repeat: no-repeat;
    clear: both;

    h3 {
      font-family: $Courgette-Font;
      font-size: 60px;
    }

    h1 {
      font-family: Poppins;
      font-size: 80px;
      font-weight: 900;
      letter-spacing: 10px;
    }

    .btn {
      font-family: Montserrat;
      font-size: 15px;
      background-color: white;
      color: $Main-Color;
      cursor: pointer;
      transition: all .3s ease-in-out;
    }

    .btn:hover {
      background-color: $Main-Color;
      color: white;
      transition: all .3s ease-in-out;

    }
  }

  .main-pepper {
    background-image: url('../../Imgs/slide1-01.jpg.webp');
  }

  .pepper-2 {
    background-image: url('../../Imgs/master-slides-02.jpg.webp');
  }

  .pepper-3 {
    background-image: url('../../Imgs/master-slides-01.jpg.webp');
  }

  .swiper-button-next::after,
  .swiper-button-prev::after {
    font-size: 15px !important;
    color: rgb(203, 202, 202) !important;
  }

  .swiper-button-next,
  .swiper-button-prev {
    padding: 35px;
    background-color: rgba(0, 0, 0, 0.4);
    border-radius: 50%;
    transition: all .3s ease-in-out;
    opacity: 0;
  }

  .swiper-button-next:hover,
  .swiper-button-prev:hover {
    background-color: rgba(255, 0, 0, 0.3);
    transition: all .3s ease-in-out;
  }
}

.swiper:hover {

  .swiper-button-next,
  .swiper-button-prev {
    opacity: 1;
    transition: all .3s ease-in-out;
  }
}
@media only screen and (max-width:426px) {
  .swiper-button-next,
  .swiper-button-prev {
    padding: 25px !important;
  } 
}
</style>
