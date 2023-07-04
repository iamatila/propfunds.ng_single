<template>
  <div class="container">
    <div class="container-two" v-if="totalValue">
      <p>Investment calculator</p>
      <div class="con">
        <div class="column">
          <p>Total Returns</p>
          <h3>N {{ totalValue.Total_returns || "0" }}</h3>

          <p>Percentage Interest</p>
          <h4>{{ totalValue.interest || "0" }} %</h4>
        </div>
        <div class="column don">
          <Donut v-if="totalValue" :totalValues="totalValue" />
          <div class="joint">
            <p>Your Investment</p>
            <h3>N {{ totalValue.inital_investment || "0" }}</h3>
          </div>
        </div>
      </div>
      <div class="labels">
        <div class="grp">
          <img src="@/assets/insurance.png" alt="" id="insurance" />
          <label for="insurance">Insurance</label>
        </div>

        <div class="grp">
          <img src="@/assets/tax.png" alt="" id="tax" />
          <label for="tax">Taxes</label>
        </div>

        <div class="grp">
          <img src="@/assets/commission.png" alt="" id="comm" />
          <label for="comm">Commission</label>
        </div>
      </div>
      <!-- <div class="txt">
        <h6>N {{ totalValue.insurance || "0" }}</h6>
        <h6>N {{ totalValue.taxes || "0" }}</h6>
        <h6>N {{ totalValue.commission || "0" }}</h6>
      </div> -->
    </div>

    <div class="container-two" v-else>
      <p>Investment calculator</p>
      <div class="con">
        <div class="column">
          <p>Total Returns</p>
          <h3>N 0</h3>

          <p>Percentage Interest</p>
          <h4>0 %</h4>
        </div>
        <div class="column don"></div>
      </div>
      <div class="labels">
        <div class="grp">
          <img src="@/assets/insurance.png" alt="" id="insurance" />
          <label for="insurance">Insurance</label>
        </div>

        <div class="grp">
          <img src="@/assets/tax.png" alt="" id="tax" />
          <label for="tax">Taxes</label>
        </div>

        <div class="grp">
          <img src="@/assets/commission.png" alt="" id="comm" />
          <label for="comm">Commission</label>
        </div>
      </div>
    </div>

    <div class="wrapper">
      <!-- <button>Go to school</button> -->
      <p>Slots</p>
      <Slider
        v-model="slotNo.value"
        :min="1"
        :max="50"
        :format="slotNo.format"
        class="slidercolor"
      />
      <!-- <span>{{ slotNo.value }}</span> -->
      <!-- <Slider v-model="slotNo.value" v-bind="slotNo"></Slider> -->
      <div
        v-if="locations && locations.places && locations.places.length"
        class="g"
      >
        <p>Location</p>
        <Slider
          v-model="exampleValue"
          :min="0"
          :max="exampleMax"
          :format="format"
          class="slidercolor"
        />
        <!-- <p>format : {{ format(exampleValue) }}</p> -->
        <!-- <span>{{ format(exampleValue) }}</span> -->
        <!-- <span>{{ this.joe }}</span> -->
      </div>

      <!-- <Slider v-model="example.value" v-bind="example" />
      <span>{{ options[example.value] }}</span> -->

      <!-- <p>Time</p> -->
      <p>Time (months)</p>
      <Slider
        v-model="exampleValue2"
        :min="0"
        :max="sliderTime.max"
        :format="format2"
        class="slidercolor"
      />
      <!-- <Slider v-model="sliderTime.value" v-bind="sliderTime" /> -->
      <!-- <span>{{ format2(exampleValue2) }}</span> -->
      <!-- <span>{{ this.jane }}</span> -->

      <p>Property Type (apartment)</p>
      <Slider
        v-model="exampleValue3"
        :min="0"
        :max="sliderProperties.max"
        :format="format3"
        class="slidercolor"
      />
      <!-- <span>{{ format3(exampleValue3) }}</span> -->
      <!-- <span>{{ this.john }}</span> -->
      <!-- <Slider v-model="sliderProperties.value" v-bind="sliderProperties" /> -->

      <!-- <span>{{ this.calc }}</span> -->
    </div>
  </div>
</template>

<style src="@vueform/slider/themes/default.css"></style>
<!-- importing default slider css -->

<script>
import Donut from "./Donut.vue";
// import CustomSlider from "vue-custom-range-slider/src/components/CustomRangeSlider.vue";
// import the styling, css or scss
// import "vue-custom-range-slider/dist/vue-custom-range-slider.css";
import axios from "axios";
import Slider from "@vueform/slider"; //importing slider
//                  index:0    index:1   index:2  index:3   index:4
// const yo = locations.places;
// const difficulties = ["Yaba", "Egbeda", "Ikoyi", "Lekki", "Festac"]; // defining base array
const time = ["6", "12", "18", "24", "30", "36", "42", "48"]; // defining base array
const property = ["1", "2", "3", "4", "5"]; // defining base array
const that = this;
export default {
  name: "Calculator",
  data() {
    return {
      numb: null,
      exampleMax: null,
      exampleValue: 0,
      exampleValue2: 1,
      exampleValue3: 3,
      locations: [],
      markers: [],
      arrMarkers: [],
      sliderLocation: [],
      optionsTime: time,
      optionsProperties: property,
      value: 2,
      slotNo: {
        min: 1,
        max: 50,
        value: 2,
        format: function (value) {
          return `${Math.round(value)} slot`;
        },
      },
      sliderTime: {
        min: 0,
        max: 7,
        value: 2,
        // format: function (value) {
        //   return `${time[value]} months`;
        // },
      },
      sliderProperties: {
        min: 0,
        max: 4,
        value: 2,
        // format: function (value) {
        //   return `${property[value]} bedroom`;
        // },
      },
      finalLocations: "",
      calc: null,
      joe: "",
      jane: "",
      john: "",
      // options: locations.places,
      // example: {
      //   min: 0, // base array 0 = Effortless
      //   max: 4, // base array 4 = Punishing
      //   value: 2, // default value in the middle
      //   // format: function (value) {
      //   //   // arbitrary variable name to use in the next step
      //   //   // return difficulties[value]; // vue property called `options` (should be referenced with `this` keyword) and `index = example.value`
      //   //   return this.locations.places[value]; // vue property called `options` (should be referenced with `this` keyword) and `index = example.value`
      //   // },
      //   format(value) {
      //     return locations.places[value];
      //   },
      // },
    };
  },
  watch: {
    "slotNo.value"(val) {
      this.getCalculator();
      // console.log(val, "here val");
    },
    joe(valc) {
      this.getCalculator();
      // console.log(valc, "here val");
    },
    jane(valg) {
      this.getCalculator();
      // console.log(valg, "here valg");
    },
    john(valk) {
      this.getCalculator();
      // console.log(valk, "here val");
    },
  },
  computed: {
    totalValue() {
      return this.calc;
    },
  },
  components: {
    Slider,
    Donut,
  },
  created() {
    this.getLocation();
    // this.getCalculator();
  },
  methods: {
    format(value) {
      return (this.joe = this.finalLocations[value]);
    },
    format2(value) {
      return (this.jane = this.optionsTime[value]);
    },
    format3(value) {
      return (this.john = this.optionsProperties[value]);
    },
    getCalculator() {
      const payload = {
        slots: this.slotNo.value,
        time: this.jane,
        location: this.joe,
        property_type: this.john,
      };
      axios
        .post(`/calculator/`, payload)
        .then((response) => {
          this.calc = response.data;
          // console.log(this.calc, "this.calc");
        })
        .catch((error) => {
          // console.log(error, "error");
          // this.$toast.warning("Please try another by moving the slide again", {
          //   // override the global option
          //   position: "top-right",
          // });
          // setTimeout(this.$toast.clear, 2000);
        });
    },
    getLocation() {
      axios
        .get("/locations/")
        .then((response) => {
          this.locations = response.data;

          // console.log(this.locations.places, "without");

          this.finalLocations = this.locations.places.reverse();
          // this.finalLocations = this.locations.places;
          // console.log(this.finalLocations, "this.finalLocations");

          this.num = +this.locations.places.length;
          // console.log(this.num, "num");
          this.exampleMax = this.num - 1;
          // console.log(this.exampleMax, "exampleMax");
          // console.log(this.locations.places.reverse(), "this.locations");
        })
        .catch((error) => {
          // console.log(error);
        });
    },
  },
};
</script>

<style scoped>
@import "~bulma/css/bulma.css";

.slidercolor {
  --slider-tooltip-bg: #001951;
  --slider-connect-bg: #001951;
}
/* cursor: pointer; */
.container {
  width: 385px;
  height: 500px;
  border-radius: 31px;
  box-shadow: 0 0 0.5px 0.2px gray;
  /* box-shadow: grey; */
  /* border: 1px solid grey; */
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: white;
  /* margin: auto; */
  margin-top: -40px;
  cursor: pointer;
}
.container-two {
  width: 385px;
  height: 281px;
  box-shadow: 0 0 5px 5px rgba(0, 0, 0, 0.13);
  border-radius: 31px;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-image: url("~@/assets/calc-bgimg.png");
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
}
.container-two p {
  font-weight: 500;
  font-size: 10px;
  line-height: 12px;
  letter-spacing: 0.02em;
  color: #777777;
}
.wrapper {
  width: 85%;
  margin: auto;
  /* margin-top: 6px; */
  height: 239px;
  position: absolute;
  top: 270px;
}
.wrapper p {
  font-weight: 500;
  font-size: 12px;
  line-height: 15px;
  letter-spacing: 0.02em;
  color: #777777;
  text-align: left;
  margin-top: 20px;
  cursor: pointer;
}
.con {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 32px;
}
.column {
  flex-basis: 50%;
}
.labels {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  width: 100%;
}
label {
  font-weight: 500;
  font-size: 10px;
  line-height: 12px;
  letter-spacing: 0.02em;
  color: #777777;
}
.grp {
  display: flex;
  justify-content: center;
  align-items: center;
}
.labels .grp > img {
  width: 8px;
  height: 8px;
  margin-right: 4px;
}
.don {
  position: relative;
}
.joint {
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  flex-direction: column;
  top: 40px;
  right: 70px;
}
.joint > p {
  font-style: normal;
  font-weight: normal;
  font-size: 6px;
  line-height: 7px;
  text-align: center;
  color: #000000;
  width: 31px;
}
.joint > h3 {
  font-weight: 500;
  font-size: 13px;
  line-height: 16px;
  color: #001951;
  width: 60px;
  margin-top: 0;
}
.txt {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  width: 100%;
}
.txt > h6 {
  font-style: normal;
  font-weight: 500;
  font-size: 9px;
  line-height: 11px;
  text-align: center;
  letter-spacing: 0.02em;
  color: #000000;
  margin-top: 0;
}
@media only screen and (max-width: 800px) {
  .container {
    /* width: 365px; */
    width: 320px;
    height: 510px;
    border-radius: 31px;
    /* box-shadow: 0 0 0.5px 0.2px gray; */
    /* box-shadow: grey; */
    /* border: 1px solid grey; */
    /* display: flex;
  flex-direction: column;
  align-items: center;
  background-color: white; */

    /* margin: auto; */
    margin-top: -20px;
    margin-bottom: 30px;
    /* margin-left: -5px; */
    cursor: pointer;
  }
  .container-two {
    width: 320px;
    height: 281px;
    /* box-shadow: 0 0 5px 5px rgba(0, 0, 0, 0.13);
  border-radius: 31px;
  display: flex;
  flex-direction: column;
  align-items: center;

  background-image: url("~@/assets/calc-bgimg.png");
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center; */
  }
}
</style>
