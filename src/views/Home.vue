<template>
  <div>
    <MainNavbar />
    <div class="is-hidden-touch" style="margin-top: 80px">
      <div class="columns">
              <div class="column notification bG">
                <div style="margin-top: 5%; margin-bottom: 5%">
                  <div class="backG1" style="padding-left: 40px">
                    <h1
                      class="title has-text-left is-size-1"
                      style="color: #001951; margin-bottom: 40px"
                    >
                      Join Our Waitlist and be a <br /> Proptech Brailbalzer with us
                    </h1>
                    <p class="has-text-left" style="margin-bottom: 20px">
                      Join our waitlist and be a proptech pioneer. Get early access to,
                      <br />
                      game changing real estate investments.
                    </p>
                    <div class="buttons">
                      <router-link
                        :to="{ name: 'Home' }"
                        class="investButton"
                        style="text-decoration: none; color: white"
                        >Join now</router-link
                      >
                      <button
                        class="button"
                        @click="toggle()"
                        style="
                        height: 43px;
                        border-radius: 5px;
                        font-size: 16px;
                        cursor: pointer;
                        margin-top: 9px;
                        border: 1px solid #001951;
                      "
                      >
                        <img
                          src="@/assets/play-icon.png"
                          alt=""
                          style="margin-right: 10px; height: 15px; width: 15px"
                        />Watch a brief video
                      </button>
                    </div>
                  </div>
                  <div class="box"></div>

                  <div class="trailer">
                    <video
                      id="video1"
                      src="@/assets/video/video.mp4"
                      controls="true"
                    ></video>
                    <div class="close">
                      <i
                        style="color: #fff"
                        class="bx bx-x-circle"
                        @click="toggle()"
                      >
                      </i>
                    </div>
                  </div>
                </div>
              </div>
            </div>
      <!-- <div ref="container" class="keen-slider">
        <div class="keen-slider__slide number-slide1">
          <div class="columns">
            <div class="column notification bG">
              <div style="margin-top: 5%; margin-bottom: 5%">
                <div class="backG1" style="padding-left: 40px">
                  <h1
                    class="title has-text-left is-size-1"
                    style="color: #001951; margin-bottom: 40px"
                  >
                    Seamless way to invest <br /> and earn in real estate
                  </h1>
                  <p class="has-text-left" style="margin-bottom: 20px">
                    Invest in high-yield, professionally managed real estate,
                    <br />
                    with as little as NGN 25,000.
                  </p>
                  <div class="buttons">
                    <router-link
                      :to="{ name: 'Home' }"
                      class="investButton"
                      style="text-decoration: none; color: white"
                      >Invest now</router-link
                    >
                    <button
                      class="button"
                      @click="toggle()"
                      style="
                        height: 43px;
                        border-radius: 5px;
                        font-size: 16px;
                        cursor: pointer;
                        margin-top: 9px;
                        border: 1px solid #001951;
                      "
                    >
                      <img
                        src="@/assets/play-icon.png"
                        alt=""
                        style="margin-right: 10px; height: 15px; width: 15px"
                      />Watch a brief video
                    </button>
                  </div>
                </div>
                <div class="box"></div>

                <div class="trailer">
                  <video
                    id="video1"
                    src="@/assets/video/video.mp4"
                    controls="true"
                  ></video>
                  <div class="close">
                    <i
                      style="color: #fff"
                      class="bx bx-x-circle"
                      @click="toggle()"
                    >
                    </i>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="keen-slider__slide number-slide2">
          <div class="columns">
            <div class="column notification bG">
              <div style="margin-top: 5%; margin-bottom: 5%">
                <div class="backG2" style="padding-left: 40px">
                  <p
                    class="title has-text-left is-size-1"
                    style="color: #001951; margin-bottom: 40px"
                  >
                    Co-earn properties with as
                    <br />
                    low as N25,000
                  </p>
                  <p class="has-text-left" style="margin-bottom: 20px">
                    With as low as NGN 25,000, co-earn on investments in Our
                    Property Developments
                    <br />
                    to earn high returns.
                    <br />
                    <i>No hidden charges whatsoever!</i> 
                  </p>
                  <div class="buttons">
                    <router-link
                      :to="{ name: 'Home' }"
                      class="investButton"
                      style="text-decoration: none; color: white"
                      >Invest now</router-link
                    >
                    <button
                      class="button"
                      @click="toggle2()"
                      style="
                        height: 43px;
                        border-radius: 5px;
                        font-size: 16px;
                        cursor: pointer;
                        margin-top: 9px;
                        border: 1px solid #001951;
                      "
                    >
                      <img
                        src="@/assets/play-icon.png"
                        alt=""
                        style="margin-right: 10px; height: 15px; width: 15px"
                      />Watch a brief video
                    </button>
                  </div>
                </div>
                <div class="box2">
                  <Calculator />
                </div>

                <div class="trailer2">
                  <video
                    id="video2"
                    src="@/assets/video/video.mp4"
                    controls="true"
                  ></video>
                  <div class="close2">
                    <i
                      style="color: #fff"
                      class="bx bx-x-circle"
                      @click="toggle2()"
                    >
                    </i>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div v-if="slider" class="dots">
        <button
          v-for="(_slide, idx) in dotHelper"
          @click="slider.moveToIdx(idx)"
          :class="{ dot: true, active: current === idx }"
          :key="idx"
        ></button>
      </div> -->
    </div>

    <div class="is-hidden-desktop" style="margin: 25px 0">
      <div class="colu" style="margin-top: 100px">
              <div class="columns">
                <div class="column notification bG">
                  <div style="padding: 75px 0">
                    <p class="title is-size-4" style="color: #001951">
                      Join Our Waitlist and be a <br /> Proptech Brailbalzer with us
                    </p>
                    <p>
                      Join our waitlist and be a proptech pioneer. 
                      <br /> 
                      Get early access to,
                      <br />
                       game changing real estate investments.
                    </p>
                    <a @click="toggleMobile()" style="text-decoration: none">
                      <div style="margin-top: 10px; margin-bottom: 10px">
                        <span class="icon">
                          <i class="bx bx-play" style="color: red"></i>
                        </span>
                        <span style="color: black">Watch a brief video</span>
                      </div>
                    </a>
                    <div class="trailerMobile">
                      <video
                        id="video3"
                        src="@/assets/video/video.mp4"
                        controls="true"
                      ></video>
                      <div class="closeMobile">
                        <i
                          style="color: #fff"
                          class="bx bx-x-circle"
                          @click="toggleMobile()"
                        >
                        </i>
                      </div>
                    </div>
                    <br />
                    <router-link
                      :to="{ name: 'Home' }"
                      class="button"
                      style="
                      color: white;
                      background-color: #001951;
                      border: none;
                      margin-top: 10px;
                      margin-bottom: 10px;
                    "
                      >Join now
                    </router-link>
                    <!-- <div class="btn-container">
                      <div class="btn">
                        <i class="bx bxl-play-store"></i>
                        <div class="group">
                          <div class="format">Download on</div>
                          <div class="format-2">Google Play</div>
                        </div>
                      </div>
                      <div class="btn">
                        <i class="bx bxl-apple"></i>
                        <div class="group">
                          <div class="format">Get it on</div>
                          <div class="format-2">Apple Store</div>
                        </div>
                      </div>
                    </div> -->
                  </div>
                </div>
              </div>
            </div>
    </div>
    <!-- <div class="is-hidden-desktop" style="margin: 25px 0">
      <swiper
        class="parallax-slider"
        :pagination="{
          clickable: true,
        }"
        :autoplay="{
          delay: 8000,
          disableOnInteraction: true,
          stopOnLastSlide: true,
        }"
        parallax
        grabCursor
        @swiper="onSwiperInitialized"
      >
        <swiper-slide class="parallax-slide">
          <div class="colu" style="margin-top: 100px">
            <div class="columns">
              <div class="column notification bG">
                <div style="padding: 75px 0">
                  <p class="title is-size-4" style="color: #001951">
                    Seamless way to own <br />
                    a property
                  </p>
                  <p>
                    Invest in high-yield, professionally managed <br />
                    real estate, with as little as <br />
                    NGN 25,000.
                  </p>
                  <a @click="toggleMobile()" style="text-decoration: none">
                    <div style="margin-top: 10px; margin-bottom: 10px">
                      <span class="icon">
                        <i class="bx bx-play" style="color: red"></i>
                      </span>
                      <span style="color: black">Watch a brief video</span>
                    </div>
                  </a>
                  <div class="trailerMobile">
                    <video
                      id="video3"
                      src="@/assets/video/video.mp4"
                      controls="true"
                    ></video>
                    <div class="closeMobile">
                      <i
                        style="color: #fff"
                        class="bx bx-x-circle"
                        @click="toggleMobile()"
                      >
                      </i>
                    </div>
                  </div>
                  <br />
                  <router-link
                    :to="{ name: 'Home' }"
                    class="button"
                    style="
                      color: white;
                      background-color: #001951;
                      border: none;
                      margin-top: 10px;
                      margin-bottom: 10px;
                    "
                    >Invest now
                  </router-link>
                  <div class="btn-container">
                    <div class="btn">
                      <i class="bx bxl-play-store"></i>
                      <div class="group">
                        <div class="format">Download on</div>
                        <div class="format-2">Google Play</div>
                      </div>
                    </div>
                    <div class="btn">
                      <i class="bx bxl-apple"></i>
                      <div class="group">
                        <div class="format">Get it on</div>
                        <div class="format-2">Apple Store</div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </swiper-slide>

        <swiper-slide class="parallax-slide">
          <div class="colu" style="margin-top: 50px">
            <div class="columns">
              <div class="column notification bG">
                <div style="padding: 50px 0">
                  <p class="title is-size-4" style="color: #001951">
                    Co-earn properties with as <br />low as N25,000
                  </p>
                  <p class="">
                    With as low as NGN 25,000, co-earn on <br />
                    investments in Our Property Developments <br />
                    to earn high returns.<br />
                    <i>No hidden charges whatsoever!</i>
                  </p>
                  <a @click="toggleMobile2()" style="text-decoration: none">
                    <div style="margin-top: 10px; margin-bottom: 10px">
                      <span class="icon">
                        <i class="bx bx-play" style="color: red"></i>
                      </span>
                      <span style="color: black">Watch a brief video</span>
                    </div>
                  </a>
                  <div class="trailerMobile2" id="myVideo">
                    <video
                      id="video4"
                      src="@/assets/video/video.mp4"
                      controls="true"
                    ></video>
                    <div class="closeMobile2">
                      <i
                        style="color: #fff"
                        class="bx bx-x-circle"
                        @click="toggleMobile2()"
                      >
                      </i>
                    </div>
                  </div>
                  <br />
                  <router-link
                    :to="{ name: 'Home' }"
                    class="button"
                    style="
                      color: white;
                      background-color: #001951;
                      border: none;
                      margin-bottom: 5px;
                    "
                    >Invest now
                  </router-link>
                  <div class="btn-container">
                    <div class="btn">
                      <i class="bx bxl-play-store"></i>
                      <div class="group">
                        <div class="format">Download on</div>
                        <div class="format-2">Google Play</div>
                      </div>
                    </div>
                    <div class="btn">
                      <i class="bx bxl-apple"></i>
                      <div class="group">
                        <div class="format">Get it on</div>
                        <div class="format-2">Apple Store</div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </div> -->

    <!-- <div class="is-hidden-desktop">
      <div class="box3">
        <Calculator />
      </div>
    </div> -->

    <Featuredon />
    <Sliderone />
    <Slidertwo />
    <!-- <Sliderscroll /> -->
    <Lastsection />

    <Footer />
    
  </div>
</template>

<script>
import { computed, ref } from "vue";
import "keen-slider/keen-slider.min.css";
import { useKeenSlider } from "keen-slider/vue"; // import from 'keen-slider/vue.es' to get an ES module

import MainNavbar from "../components/MainNavbar.vue";
import Lastsection from "../components/Lastsection.vue";
import Footer from "../components/Footer.vue";
import Featuredon from "../components/Featuredon.vue";
import Sliderone from "../components/Sliderone.vue";
import Slidertwo from "../components/Slidertwo.vue";
import Sliderscroll from "../components/Sliderscroll.vue";
// import Calculator from "../components/Calculator.vue";

// import Swiper, { Navigation, Pagination } from 'swiper';
// // import Swiper and modules styles
// import 'swiper/css';
// import 'swiper/css/navigation';
// import 'swiper/css/pagination';
// import Swiper bundle with all modules installed
// import Swiper from 'swiper/bundle';

// import styles bundle
// import 'swiper/css/bundle';
// import Swiper JS
// import Swiper from 'swiper';
// import Swiper styles
// import 'swiper/css';

// import SwiperCore, { Controller } from "swiper";
// import { Swiper} from "swiper/esm/vue/swiper.js";
// import {SwiperSlide} from "swiper/esm/vue/swiper-slide.js";

// swiper core
// import SwiperCore, { Autoplay, Parallax } from "swiper";
// import SwiperCore, { Autoplay, Navigation, Pagination, Parallax } from "swiper";
// swiper vue
// import { Swiper, SwiperSlide } from "swiper/vue";
// import swiper css
// import "swiper/swiper.scss";
// import css for components
// navigation
// import "swiper/swiper-bundle.css";
// import "swiper/components/navigation/navigation.scss";
// font awesome icons
// import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";

// SwiperCore.use([Autoplay, Navigation, Pagination, Parallax]);
// Vue.component("font-awesome-icon", FontAwesomeIcon);

// import Meta from "vue-meta";

export default {
  name: "Home",

  data() {
    return {
      // parallaxSwiperWidth: 0,
    };
  },
  // metaInfo: {
  //   link: [{ rel: "canonical", href: "https://propfunds.ng" }],
  // },
  // mounted() {
  //   document.title = "Home || propfunds.ng";
  //   // "Seamless way to own a property, Invest in high-yield, professionally managed real estate, with as little as NGN 25,000. || Propfunds.ng";
  // },
  computed: {
    // parallaxAmount() {
    //   return this.parallaxSwiperWidth * 1.0;
    // },
  },

  methods: {
    // onSwiperInitialized(swiper) {
    //   this.parallaxSwiperWidth = swiper.width;
    // },
    toggle() {
      let trailer = document.querySelector(".trailer");
      let myVideo = document.getElementById("video1");
      trailer.classList.toggle("active");
      myVideo.pause();
      myVideo.currentTime = 0;
    },
    toggle2() {
      let trailer = document.querySelector(".trailer2");
      let myVideo = document.getElementById("video2");
      trailer.classList.toggle("active");
      myVideo.pause();
      myVideo.currentTime = 0;
    },
    toggleMobile() {
      let trailer = document.querySelector(".trailerMobile");
      let myVideo = document.getElementById("video3");
      trailer.classList.toggle("active");
      myVideo.pause();
      myVideo.currentTime = 0;
    },
    toggleMobile2() {
      let trailer = document.querySelector(".trailerMobile2");
      let myVideo = document.getElementById("video4");
      trailer.classList.toggle("active");
      myVideo.pause();
      myVideo.currentTime = 0;
    },
  },

  setup() {
    const [container] = useKeenSlider(
      {
        loop: false,
      },
      [
        (slider) => {
          let timeout;
          let mouseOver = false;
          function clearNextTimeout() {
            clearTimeout(timeout);
          }
          function nextTimeout() {
            clearTimeout(timeout);
            if (mouseOver) return;
            timeout = setTimeout(() => {
              slider.next();
            }, 8000);
          }
          slider.on("created", () => {
            slider.container.addEventListener("mouseover", () => {
              mouseOver = true;
              clearNextTimeout();
            });
            slider.container.addEventListener("mouseout", () => {
              mouseOver = false;
              nextTimeout();
            });
            nextTimeout();
          });
          slider.on("dragStarted", clearNextTimeout);
          slider.on("animationEnded", nextTimeout);
          slider.on("updated", nextTimeout);
        },
      ]
    );

    const dotHelper = computed(() =>
      slider.value
        ? [...Array(slider.value.track.details.slides.length).keys()]
        : []
    );
    return { container, dotHelper };
  },

  components: {
    Featuredon,
    Sliderone,
    Slidertwo,
    Footer,
    Sliderscroll,
    Lastsection,
    MainNavbar,
    // Calculator,

    // Swiper,
    // SwiperSlide,
    // FontAwesomeIcon,
  },
};
</script>

<style scoped>
/* @import "../../node_modules/bulma"; */
@import "~bulma/css/bulma.css";

.bG {
  background-color: white;
}
.backG1 {
  /* background-image: url(${require('@/assets/images/cards.jpg')}); */
  background-image: url("~@/assets/bg-img.png");

  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  width: 100%;
  border-radius: 30px;
  padding-top: 80px;
  padding-bottom: 80px;
}

.backG2 {
  background-image: url("~@/assets/bg-img.png");

  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  width: 100%;
  border-radius: 30px;
  padding-top: 70px;
  padding-bottom: 70px;
}

.box {
  background-image: url("~@/assets/img-s1.png");
  width: 385px;
  height: 500px;
  border-radius: 45px;
  position: absolute;
  top: 2%;
  left: 60%;
  opacity: 0.8;
  z-index: 9;
  margin: 20px;
}
.box2 {
  width: 390px;
  height: 500px;
  border-radius: 45px;
  position: absolute;
  top: 2%;
  left: 60%;
  opacity: 0.8;
  z-index: 9;
  margin: 20px;
}
.box3 {
  width: 370px;
  height: 500px;
  border-radius: 45px;
  top: 0;
  margin: auto;
}

.tre {
  background-color: rgb(215, 236, 255, 0.4);
  padding-top: 10px;
  border-radius: 10px;
}
.yt {
  cursor: pointer;
}
.parallax-slider {
  position: relative;
}
.parallax-slide {
  height: 550px !important;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  cursor: pointer;
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
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
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
.investButton {
  background: #001951;
  border-radius: 5px;
  border: 1px solid #001951;
  color: #fff;
  padding: 10px 40px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  margin-right: 5px;
  cursor: pointer;
}
.trailer {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 10000;
  background: rgba(0, 0, 0, 0.78);
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  visibility: hidden;
  opacity: 0;
}

.trailer.active {
  visibility: visible;
  opacity: 1;
}

.trailer > video {
  position: relative;
  max-width: 900px;
  outline: none;
}
.close {
  position: absolute;
  top: 30px;
  right: 30px;
  cursor: pointer;
  font-size: 24px;
}
.trailer2 {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 10000;
  background: rgba(0, 0, 0, 0.78);
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  visibility: hidden;
  opacity: 0;
}

.trailer2.active {
  visibility: visible;
  opacity: 1;
}

.trailer2 > video {
  position: relative;
  max-width: 900px;
  outline: none;
}
.close2 {
  position: absolute;
  top: 30px;
  right: 30px;
  cursor: pointer;
  font-size: 24px;
}
.trailerMobile {
  position: absolute;
  top: 55%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 10000;
  background: rgba(0, 0, 0, 0.78);
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  visibility: hidden;
  opacity: 0;
}

.trailerMobile.active {
  visibility: visible;
  opacity: 1;
}

.trailerMobile > video {
  position: relative;
  max-width: 900px;
  outline: none;
}

.closeMobile {
  position: absolute;
  top: 10px;
  right: 80px;
  cursor: pointer;
  font-size: 24px;
  margin-top: -100px;
}

.trailerMobile2 {
  position: absolute;
  top: 55%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 10000;
  background: rgba(0, 0, 0, 0.78);
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  visibility: hidden;
  opacity: 0;
}

.trailerMobile2.active {
  visibility: visible;
  opacity: 1;
}

.trailerMobile2 > video {
  position: relative;
  max-width: 900px;
  outline: none;
}

.closeMobile2 {
  position: absolute;
  top: 10px;
  right: 80px;
  cursor: pointer;
  font-size: 24px;
  margin-top: -120px;
}
.btn-container {
  width: 100%;
  display: flex;
  padding-left: 20px;
}
.btn-container > .btn {
  display: flex;
  margin: 7% 0;
  background-color: #001951;
  border: none;
  border-radius: 5px;
  color: white;
  font-family: "Quicksand", sans-serif;
  font-size: 14px;
  cursor: pointer;
  height: 30px;
  width: 140px;
  align-items: center;
  justify-content: center;
  padding: 8px 0;
  margin-right: 20px;
}

.btn-container > .btn > i {
  font-size: 28px;
}
.group {
  margin-left: 10px;
}
.group > .format {
  font-weight: 500;
  font-size: 10px;
  line-height: 12px;
}
.group > .format-2 {
  font-weight: 400;
  font-size: 14px;
}

@media only screen and (max-width: 800px) {
  * {
    margin: 0;
  }
  .cover {
    width: 100%;
    background-color: rgba(120, 121, 241, 0.6);
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 1em;
  }
  .bG {
    background-image: url("~@/assets/bGmobile.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  .button2 {
    width: 400px;
    margin-left: 65px;
  }
  .colu {
    padding: auto;
  }
  .box3 {
    margin: auto;
    width: 320px;
  }

  .col-2 > img {
    display: none;
  }
  .trailer > video {
    max-width: 90%;
  }
  .trailer2 > video {
    max-width: 90%;
  }
  .close {
    top: 14rem;
    color: #000000;
  }
  .yt {
    display: none;
  }

  /* Mobile View CSS */
  .ty {
    display: block;
  }
  .tyC {
    display: block;
    margin-top: 85px;
  }
  .trailerMobile > video {
    max-width: 70%;
  }
  .trailerMobile2 > video {
    max-width: 70%;
  }
  .closeMobile {
    top: 14rem;
    color: #000000;
  }
  .closeMobile2 {
    top: 14rem;
    color: #000000;
  }
  .container-1 {
    width: 100%;
    background-color: rgba(120, 121, 241, 0.16);
    border-radius: 8px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 1em;
  }

  .container-flex {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    padding: 1em 1em;
    margin-bottom: 1em;
  }
  .container-flex p {
    font-family: "Quicksand", sans-serif;
    font-weight: normal;
    font-size: 1rem;
    line-height: 20px;
    text-align: center;
    color: #484848;
    margin: 20px 0;
  }
  .container-flex h3 {
    font-family: "Quicksand", sans-serif;
    font-weight: bold;
    font-size: 24px;
    line-height: 32px;
    text-align: center;
    letter-spacing: 0.02em;
    color: #5d5fef;
  }
  .container-flex a {
    cursor: pointer;
    text-decoration: none;
  }

  .dis {
    justify-content: space-between;
    margin-bottom: 5px;
  }
  .dis a {
    text-decoration: none;
  }
  .dis > a > i {
    font-size: 20px;
    color: #fc573b;
  }
  .dis > span {
    padding-left: 4px;
    font-family: "Quicksand" sans-serif;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 20px;

    color: #000000;
  }


  .fmt-button {
    border: 2px solid #001951;
    color: #001951;
    background-color: #fff;
    border-radius: 5px;
    padding: 14px 4em;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
  }
  .fmt-button-Mobile {
    border: 2px solid #001951;
    background: #001951;
    border-radius: 5px;
    border: none;
    color: #fff;
    padding: 16px 3em;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 0 2px;
    cursor: pointer;
  }
}
</style>
