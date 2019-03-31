<template>
  <div class="w-full md:w-1/2 p-3">
    <div class="bg-white border rounded shadow">
      <div class="border-b p-3">
        <h5 class="uppercase text-grey-dark">Graph</h5>
      </div>
      <div class="p-5">
        <BarChart :height="200" :options="options" :chartdata="chartdata" />
      </div>
    </div>
  </div>
</template>

<script>
import BarChart from '~/components/charts/BarChart.vue';

export default {
  components: {
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
