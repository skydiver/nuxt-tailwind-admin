<template>
  <div class="w-full md:w-1/2 p-3">
    <Box title="Graph">
      <BarChart :height="200" :options="options" :chartdata="chartdata" />
    </Box>
  </div>
</template>

<script>
import Box from '~/components/containers/Box.vue';
import BarChart from '~/components/charts/BarChart.vue';

export default {
  components: {
    Box,
    BarChart
  },
  data() {
    return {
      options: {
        scales: {
          yAxes: [
            {
              ticks: {
                beginAtZero: true
              }
            }
          ]
        }
      },
      chartdata: {
        labels: ['January', 'February', 'March', 'April'],
        datasets: [
          {
            label: 'Page Impressions',
            data: [10, 20, 30, 40],
            borderColor: 'rgb(255, 99, 132)',
            backgroundColor: 'rgba(255, 99, 132, 0.2)'
          },
          {
            label: 'Adsense Clicks',
            data: [5, 15, 10, 30],
            type: 'line',
            fill: false,
            borderColor: 'rgb(54, 162, 235)'
          }
        ]
      }
    };
  }
};
</script>
