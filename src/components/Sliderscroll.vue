<template>
  <div class="sliderr">
    <h2 class="txt">OUR TOP INVESTMENTS</h2>

    <div class="carousel">
      <!-- <swiper class="parallax-slider" :navigation="{ nextEl: '.nextArrow', prevEl: '.prevArrow' }" parallax grabCursor
        @swiper="onSwiperInitialized">
        <div class="parallax-slider-navigation">
          <div class="nav-indicator prevArrow">
            <font-awesome-icon :icon="['fas', 'chevron-left']" />
          </div>
          <div class="nav-indicator nextArrow">
            <font-awesome-icon :icon="['fas', 'chevron-right']" />
          </div>
        </div>
        <swiper-slide class="parallax-slide" v-for="CoEarn in CoEarnListview" :key="CoEarn.id">
          <div class="parallax-slide-image" :data-swiper-parallax="parallaxAmount" :data-swiper-parallax-opacity="0.5">
            <div>
            <img :src="CoEarn.thumbnail" alt="" class="img" />
              <h3>{{ CoEarn.location }}</h3>
              <p class="text">{{ CoEarn.about }}</p>
            </div>
          </div>
        </swiper-slide>
      </swiper> -->
    </div>
  </div>
</template> 

<script>
// import Swiper JS
// import Swiper from 'swiper';
// // import Swiper styles
// import 'swiper/css';
// // core version + navigation, pagination modules:
// // import Swiper, { Navigation, Pagination } from 'swiper';
// // import Swiper and modules styles
// import 'swiper/css';
// import 'swiper/css/navigation';
// import 'swiper/css/pagination';
// import Swiper bundle with all modules installed
// import Swiper from 'swiper/bundle';

// import styles bundle
// import 'swiper/css/bundle';

// // swiper core
// import SwiperCore, { Navigation, Parallax } from "swiper";
// // swiper vue
// // import { Swiper, SwiperSlide } from "swiper/vue";
// // import { Swiper, SwiperSlide } from "swiper/vue/swiper-vue.js";
// import { Swiper } from "swiper/esm/vue/swiper.js";
// import { SwiperSlide } from "swiper/esm/vue/swiper-slide.js";
// // import swiper css
// // import "swiper/swiper.scss";
// // import css for components
// // navigation
// import "swiper/swiper-bundle.css";
// // import "swiper/components/navigation/navigation.scss";
// // font awesome icons
// // import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";

// SwiperCore.use([Navigation, Parallax]);

import axios from "axios";

export default {
  name: "Autoplay",
  components: {
    // Swiper,
    // SwiperSlide,
    // FontAwesomeIcon,
  },
  data(){
    return {
      CoEarnListview: [],
    }
  },
  mounted() {
    // (document.title = "CoEarn | Propfunds.ng"),
    this.getCoEarnListview()
  },
  methods: {
    getCoEarnListview() {
      axios
        .get("/coearnlist/")
        .then((response) => {
          // this.CoEarnListview = response.data;
          const s = response.data;
          console.log(s, 's');
          const size = 3;
          const item = s.slice(0, size)
          // const f = s[0, 1, 2]
          console.log(item, 'item');
          this.CoEarnListview = item;
          // console.log(idCoEarn)
        })
        .catch((error) => {
          // console.log(error);
        });
    },
  }
};
</script>
<style scoped>
@import "~bulma/css/bulma.css";

.parallax-slider {
  position: relative;
}

.parallax-slide {
  height: 600px !important;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}

.parallax-slider-navigation {
  position: absolute;
  top: 50%;
  z-index: 2;
  left: 0;
  right: 0;
  margin: auto;
  display: flex;
  justify-content: space-between;
  height: 0;
}

.parallax-slide-image {
  height: 100%;
  width: 100%;
  /* position: absolute; */
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
}
.parallax-slide-image2 {
  height: 100%;
  width: 100%;
  /* position: absolute; */
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
}

.nav-indicator {
  height: 40px;
  width: 40px;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  background-color: #001951;
  color: white;
  border-radius: 40px;
  cursor: pointer;
  position: relative;
  transform: translateY(-50%);
}
.img {
  width: 500px;
  height: 300px;
}
.text {
  width: 527px;
  /* text-align: left; */
  font-size: 14px;
  line-height: 17px;
  letter-spacing: 0.02em;
  color: #000000;
}
.caption {
  font-size: 22px;
  line-height: 27px;
  letter-spacing: 0.02em;
  color: #000000;
  text-align: left;

  margin-bottom: -10px;
}
.txt {
  font-style: normal;
  font-weight: bold;
  font-size: 32px;
  line-height: 56px;
  letter-spacing: 0.02em;
  color: #000000;
}
@media only screen and (max-width: 800px) {
  
  .carousel__slide--next > .carousel__item {
    transform: scale(0) translate(-80px);
    /* padding-right: 150px; */
  }
  .carousel__slide--prev > .carousel__item {
    transform: scale(0) translate(10px);
    /* visibility: hidden; */
  }
  .sliderr {
    /* width: 330px; */
    /* height: 160px; */
    margin: auto;
    justify-content: center;
    /* margin-left: 10px; */
  }
  /* .carousel__item{

  } */

  .carousel__slide > .carousel__item {
    transform: scale(0);
    opacity: 0.5;
    transition: 0.5s;
    margin-top: 24px;
    /* margin-left: -5px; */
  }
  .carousel__slide--visible > .carousel__item {
    opacity: 1;
    transform: rotateY(0);
  }
}
@media only screen and (max-width: 800px) {
  .parallax-slide {
      height: 500px !important;
    }
  .img {
    width: 350px;
    height: 250px;
  }
  .text {
    width: 350px;
    /* text-align: left; */
    font-size: 14px;
    line-height: 17px;
    letter-spacing: 0.02em;
    color: #000000;
  }
  .page {
    /* margin: auto; */
    margin-right: 50px;
  }
}
</style>
