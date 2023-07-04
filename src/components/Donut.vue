<template>
  <div>
    <apexchart
      width="200"
      type="donut"
      :options="options"
      :series="home"
    ></apexchart>
    <!-- :series="series" -->
    <!-- {{
      Object.values(totalValues)
        .map((x) => Number(x))
        .splice(1, 5)
    }}
    {{ home }} -->
  </div>
</template>

<script>
import VueApexCharts from "vue3-apexcharts";
export default {
  props: ["totalValues"],
  components: {
    apexchart: VueApexCharts,
  },
  data: function () {
    return {
      options: {
        labels: [
          // "Commission",
          // "Insurance",
          // "Interest",
          // "Taxes",
          "ROI",
          "Interest",
          "Inital Investment",
          // "Total Returns",
        ],
        legend: {
          show: false,
        },
        dataLabels: {
          enabled: false,
        },
        colors: [
          // "#f8ea29",
          "#F44336",
          "#0e5100",
          "#001951",
          // "#440051",
          // "#9C27B0",
        ],
        responsive: [
          {
            breakpoint: 280,
            options: {
              chart: {
                width: 200,
              },
              legend: {
                show: false,
              },
            },
          },
        ],
      },
      // series: Object.values({...this.totalValues}).map((x) => Number(x)),
      // series: yourFinalValue,
      // series: undefined,
      // series: [449, 550, 41, 78, "130", 650].map((x) => Number(x)),
    };
  },
  computed: {
    yourFinalValue() {
      // console.log(this.totalValues, "total values");
      let bro =
        this.totalValues.Total_returns - this.totalValues.inital_investment;
      // console.log(bro, "bro");
      let bro2 = parseInt(this.totalValues.interest);
      // console.log(bro2, "bro2");
      // let bro3 = this.totalValues.Total_returns;
      let bro3 = this.totalValues.inital_investment;
      let bro4 = [bro, bro2, bro3];
      // console.log(bro4, "bro4");
      // return (this.series = Object.values(this.totalValues)
      //   .map((x) => Number(x))
      //   .splice(1, 3));
      return bro4;
    },
    home() {
      const yo = this.yourFinalValue;
      // const now = yo.splice(1, 2);
      // console.log(yo, "yo yo yo yo");
      // console.log(now, "now now now now");
      return yo;
    },
  },
};
</script>

<style scoped></style>
