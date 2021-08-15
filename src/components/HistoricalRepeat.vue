<template>
  <div>
    <highcharts :constructor-type="'waterfall'" :options="chartOptions"></highcharts>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      chartOptions: {
        chart: {
          // type: 'waterfall'
        },
        title: {
          text: 'Highcharts stacked waterfall',
          style: { "font-family": "Gill sans", "font-size": "26px" }
        },
        plotOptions: {
          series: {
            stacking: 'normal'
          }
        },
        series: [{
          // type: 'waterfall',
          data: [20, 10, {
            isIntermediateSum: true
          }, -15, 30, {
              isSum: true
            }]
        }, {
          // type: 'waterfall',
          data: [20, 50, {
            isIntermediateSum: true
          }, -25, 10, {
              isSum: true
            }],
          lineWidth: 0
        }, {
          // type: 'waterfall',
          data: [5, 10, {
            isIntermediateSum: true
          }, -5, 10, {
              isSum: true
            }],
          lineWidth: 0
        }]
      },
    };
  },
  mounted() { },
  methods: {
    myCallback() {
      console.log("this is callback function");
    },
  },
};
</script>

<style>
.highcharts-container {
	width: 600px;
	height: 520px;
	border: 1px solid #ddd;
	margin: auto;
}
</style>
