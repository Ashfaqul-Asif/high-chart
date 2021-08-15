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
          type: "spline",
          scrollablePlotArea: {
            minWidth: 600,
            scrollPositionX: 1,
          },
        },
        title: {
          text: "Revenue Retention by cohort",
          align: "left",
          style: { "font-family": "Gill sans", "font-size": "26px" }
        },

        yAxis: {
          title: {
            text: "Percent Cumulative Survival",
            style: { "font-family": "Gill sans", "font-size": "21px" }
          },
          minorGridLineWidth: 0,
          gridLineWidth: 0,
          alternateGridColor: null,
          max: 100,
        },

        xAxis: {
          title: {
            text: "Months Since Joining",
          },
          accessibility: {
            rangeDescription: "Range: 2010 to 2017",
          },
        },
        plotOptions: {
          spline: {
            lineWidth: 4,
            states: {
              hover: {
                lineWidth: 5,
              },
            },
            marker: {
              enabled: false,
            },
          },
        },
        legend: {
          layout: "horizontal",
          verticalAlign: "bottom",
          align: "right",
        },

        plotOptions: {
          series: {
            label: {
              connectorAllowed: false,
            },
            pointStart: 2010,
          },
        },
        plotOptions: {
          spline: {
            lineWidth: 4,
            states: {
              hover: {
                lineWidth: 5,
              },
            },
            marker: {
              enabled: false,
            },
          },
        },
        series: [
          {
            name: "2018",
            type: "spline",
            color: "#4B4BE6",
            data: [100, 85, 56, 10],
          },
          {
            name: "2019",
            type: "spline",
            color: "#BD10E0",
            data: [100, 46, 7],
          },
          {
            name: "2020",
            type: "spline",
            color: "#6297AB",
            data: [100, 11],
          },
          {
            name: "2021",
            type: "spline",
            color: "#F1C40F",
            data: [100],
          },
        ],

        responsive: {
          rules: [
            {
              condition: {
                maxWidth: 500,
              },
              chartOptions: {
                legend: {
                  layout: "horizontal",
                  align: "center",
                  verticalAlign: "bottom",
                },
              },
            },
          ],
        },
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
