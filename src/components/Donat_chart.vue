<template>
  <div>
    <br><br>
    <apexchart type="donut" width="400" :options="chartOptions" :series="series"></apexchart>
  </div>
</template>

<script>
export default {
  name: "Donat_chart",
  data() {
    return{
      series: [44, 55, 41, 17, 15],
          chartOptions: {
            chart: {
              type: 'donut',
            },
            responsive: [{
              breakpoint: 480,
              options: {
                chart: {
                  width: 200
                },
                legend: {
                  position: 'bottom'
                }
              }
            }]
          },
    };
  }
}
</script>

<style>

</style>