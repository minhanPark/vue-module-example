<template>
  <canvas ref="myLineChart" id="myLineChart"></canvas>
</template>

<script>
export default {
  mounted() {
    // var ctx = document.getElementById("myLineChart").getContext("2d");
    var ctx = this.$refs.myLineChart.getContext("2d");
    var chart = new this.$_Chart(ctx, {
      // The type of chart we want to create
      type: "line",

      // The data for our dataset
      data: {
        labels: [
          "January",
          "February",
          "March",
          "April",
          "May",
          "June",
          "July",
        ],
        datasets: [
          {
            label: "My First dataset",
            backgroundColor: "rgb(255, 99, 132)",
            borderColor: "rgb(255, 99, 132)",
            data: [0, 10, 5, 2, 20, 30, 45],
          },
        ],
      },

      // Configuration options go here
      options: {},
    });
    chart;
  },
};
</script>

<style></style>
