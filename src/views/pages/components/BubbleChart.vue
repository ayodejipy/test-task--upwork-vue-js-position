<template>
  <canvas id="bubble-chart" class="chart-canvas" height="140" />
</template>

<script>
import Chart from "chart.js/auto";
export default {
  name: "BarChart",
  mounted() {
    // Bubble chart
    var ctx8 = document.getElementById("bubble-chart").getContext("2d");

    new Chart(ctx8, {
      type: "bubble",
      data: {
        labels: ["0", "10", "20", "30", "40", "50", "60", "70", "80", "90"],
        datasets: [
          {
            label: "Dataset 1",
            data: [
              {
                x: 100,
                y: 0,
                r: 10,
              },
              {
                x: 60,
                y: 30,
                r: 20,
              },
              {
                x: 40,
                y: 350,
                r: 10,
              },
              {
                x: 80,
                y: 80,
                r: 10,
              },
              {
                x: 20,
                y: 30,
                r: 15,
              },
              {
                x: 0,
                y: 100,
                r: 5,
              },
            ],
            backgroundColor: "#cb0c9f",
          },
          {
            label: "Dataset 2",
            data: [
              {
                x: 70,
                y: 40,
                r: 10,
              },
              {
                x: 30,
                y: 60,
                r: 20,
              },
              {
                x: 10,
                y: 300,
                r: 25,
              },
              {
                x: 60,
                y: 200,
                r: 10,
              },
              {
                x: 50,
                y: 300,
                r: 15,
              },
              {
                x: 20,
                y: 350,
                r: 5,
              },
            ],
            backgroundColor: "#3A416F",
          },
        ],
      },
      options: {
        responsive: true,
        plugins: {
          legend: {
            display: false,
          },
        },
        scales: {
          y: {
            grid: {
              drawBorder: false,
              display: true,
              drawOnChartArea: true,
              drawTicks: false,
              borderDash: [5, 5],
            },
            ticks: {
              display: true,
              padding: 10,
              color: "#b2b9bf",
              font: {
                size: 11,
                family: "Open Sans",
                style: "normal",
                lineHeight: 2,
              },
            },
          },
          x: {
            grid: {
              drawBorder: false,
              display: true,
              drawOnChartArea: true,
              drawTicks: false,
              borderDash: [5, 5],
            },
            ticks: {
              display: true,
              color: "#b2b9bf",
              padding: 10,
              font: {
                size: 11,
                family: "Open Sans",
                style: "normal",
                lineHeight: 2,
              },
            },
          },
        },
      },
    });
  },
};
</script>
