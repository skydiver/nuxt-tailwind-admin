<template>
  <div class="w-full md:w-1/2 xl:w-1/3 p-3">
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
        labels: [
          'January',
          'February',
          'March',
          'April',
          'May',
          'June',
          'July'
        ],
        datasets: [
          {
            label: 'Likes',
            data: [65, 59, 80, 81, 56, 55, 40],
            fill: false,
            backgroundColor: [
              'rgba(255, 99, 132, 0.2)',
              'rgba(255, 159, 64, 0.2)',
              'rgba(255, 205, 86, 0.2)',
              'rgba(75, 192, 192, 0.2)',
              'rgba(54, 162, 235, 0.2)',
              'rgba(153, 102, 255, 0.2)',
              'rgba(201, 203, 207, 0.2)'
            ],
            borderColor: [
              'rgb(255, 99, 132)',
              'rgb(255, 159, 64)',
              'rgb(255, 205, 86)',
              'rgb(75, 192, 192)',
              'rgb(54, 162, 235)',
              'rgb(153, 102, 255)',
              'rgb(201, 203, 207)'
            ],
            borderWidth: 1
          }
        ]
      }
    };
  }
};
</script>

<style scoped></style>
