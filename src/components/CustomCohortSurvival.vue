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
          text: 'Customer Cohort Survival / Subsequent Retention',
          align: 'left',
          style: { "font-family":"Gill sans","font-size":"26px" }
        },

        subtitle: {
          text: 'This chart shows how customers survive from their first month to the next.',
          align: 'left',
          style: { "font-family":"Gill sans","font-size":"21px" }
        },

        yAxis: {
          title: {
            text: 'Percent Cumulative Survival'
          },
          minorGridLineWidth: 0,
          gridLineWidth: 0,
          alternateGridColor: null,
          max: 100
        },

        xAxis: {
          title: {
            text: 'Months Since Joining'
          },
          accessibility: {
            rangeDescription: 'Range: 2010 to 2017'
          }
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
        legend: {
          layout: 'horizontal',
          verticalAlign: 'bottom'
        },

        plotOptions: {
          series: {
            label: {
              connectorAllowed: false
            },
            pointStart: 2010
          }
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
          name: '2018',
          type: 'spline',
          color: '#4B4BE6',
          data: [
            100,
            76,
            73.7,
            72.2,
            69.8,
            67.7,
            65.3,
            61.6,
            60.1,
            58.2,
            55.8,
            53.4,
            52.1,
            49.5,
            48.2,
            46.8,
            44.8,
            43.4,
            42.1,
            40,
            38.6,
            36.6,
            34.8,
            33.3,
            31.6
          ]
        }, {
          name: '2019',
          type: 'spline',
          color: '#BD10E0',
          data: [
            100,
            53.3,
            47.3,
            45.6,
            43.3,
            41,
            38.6,
            35.6,
            33.6,
            32.1,
            30.4,
            28.1,
            26.2,
            23.6,
            21.8,
            20.2,
            17.2,
            14.6,
            12.9,
            10.6,
            9,
            7.2,
            5.6,
            4.2,
            3,
          ]
        }, {
          name: '2020',
          type: 'spline',
          color: '#6297AB',
          data: [
            100,
            52.8,
            45.6,
            43.6,
            40.7,
            37.7,
            34.6,
            31,
            28.4,
            26.3,
            22.6,
            17,
            12.8,
            6.2,
            2.5,
            0.6,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0
          ]
        }, {
          name: '2020-Q2',
          type: 'spline',
          color: '#F1C40F',
          data: [
            100,
            54.1,
            44.9,
            42.6,
            39.5,
            36,
            32,
            26.2,
            21.5,
            17.5,
            10.6,
            4.1,
            0.4,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0
          ]
        },
        {
          name: '2020-Q3',
          type: 'spline',
          color: '#14453D',
          data: [
            100,
            44.2,
            37.9,
            35.9,
            32,
            27,
            20.9,
            10.4,
            2.8,
            0.6,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0
          ]
        },
        {
          name: '2020-Q4',
          type: 'spline',
          color: '#9B7A99',
          data: [
            100,
            41.6,
            27.7,
            24.1,
            13.7,
            5,
            0.9,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0
          ]
        },
        {
          name: '2021-Q1',
          type: 'spline',
          color: '#9F8082',
          data: [
            100,
            24.9,
            4.5,
            1,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0
          ]
        },
        {
          name: '2021-Q2',
          type: 'spline',
          color: '#F1BF98',
          data: [
            100,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0,
            0

          ]
        },
        {
          name: 'Average',
          type: 'spline',
          color: '#A5243D',
          data: [
            100,
            61.7,
            56.4,
            54.6,
            51.7,
            49.1,
            46.4,
            42.6,
            40.5,
            38.8,
            36.6,
            34.1,
            32.5,
            30.1,
            28.8,
            27.5,
            25.7,
            24.3,
            23.2,
            21.6,
            20.4,
            19,
            17.7,
            16.6,
            15.5
          ]
        }

        ],

        responsive: {
          rules: [{
            condition: {
              maxWidth: 500
            },
            chartOptions: {
              legend: {
                layout: 'horizontal',
                align: 'center',
                verticalAlign: 'bottom'
              }
            }
          }]
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
.highcharts-container {
	width: 600px;
	height: 520px;
	border: 1px solid #ddd;
	margin: auto;
}
</style>
