<template>
  <div>
    <highcharts :options="chartOptions"></highcharts>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      chartOptions: {
        chart: {
          type: 'spline',
          scrollablePlotArea: {
            minWidth: 600,
            scrollPositionX: 1
          }
        },
        title: {
          text: 'Customer Lifetime Revenue (5 Year) by Monthly Cohorts',
          align: 'left',
          style: { "font-family": "Gill sans", "font-size": "26px" }

        },
        subtitle: {
          text: 'Mean & Median',
          align: 'left',
          style: { "font-family": "Gill sans", "font-size": "21px" }

        },
        xAxis: {

          // categories: ['Jul\'18', 'Oct\'18', 'Jan\'18', 'Apr\'18', 'Jul\'18', 'Oct\'18',
          //   'Jan\'18', 'Apr\'18', 'Jul\'18', 'Oct\'18', 'Jan\'18','Apr\'18'
          // ]
        },
        yAxis: {
          title: {
            text: 'Wind speed (m/s)'
          },
          minorGridLineWidth: 0,
          gridLineWidth: 0,
          alternateGridColor: null,
        },
        tooltip: {
          valueSuffix: ' m/s'
        },
        plotOptions: {
          spline: {
            lineWidth: 4,
            states: {
              hover: {
                lineWidth: 5
              }
            },
            marker: {
              enabled: false
            },

          }
        },

        series: [{
          name: 'Mean',
          color: '#4B4BE6',
          data: [113,
            101.5,
            86.1,
            74.2,
            72.3,
            67.5,
            63.1,
            64.1,
            66.8,
            63.2,
            62.6,
            60.1,
            60.3,
            61.6,
            64.5,
            59.8,
            59.7,
            61.6,
            65,
            61.6,
            64.2,
            66.5,
            68.7,
            71.4,
            75.4,
            72.8,
            240.9,
            76.2,
            59.5,
            69.8,
            74.2,
            77.7,
            76,
            80.1,
            79.9,
            75.3]

        }, {
          name: 'Median',
          color: '#BD10E0',
          data: [71.6,
            66,
            56.2,
            46.2,
            44.3,
            40.8,
            35.7,
            36.9,
            34.9,
            33,
            33.6,
            32,
            34.2,
            34.3,
            34.5,
            33.7,
            34.2,
            33.9,
            38.5,
            38.9,
            39,
            40.1,
            44.2,
            47.3,
            45.5,
            49.3,
            56.3,
            56.5,
            37.7,
            51.7,
            58.1,
            62.3,
            65.5,
            75,
            75.1,
            61.5]
        }],
        navigation: {
          menuItemStyle: {
            fontSize: '10px'
          }
        }
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
/* .highcharts-container {
	width: 600px;
	height: 520px;
	border: 1px solid #ddd;
	margin: auto;
} */
</style>
