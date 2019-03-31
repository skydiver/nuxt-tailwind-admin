<template>
  <div class="w-full md:w-1/2 p-3">
    <div class="bg-white border rounded shadow">
      <div class="border-b p-3">
        <h5 class="uppercase text-grey-dark">Graph</h5>
      </div>
      <div class="p-5">
        <LineChart :height="200" :options="options" :chartdata="chartdata" />
      </div>
    </div>
  </div>
</template>

<script>
import LineChart from '~/components/charts/LineChart.vue';

export default {
  components: {
    LineChart
  },
  data() {
    return {
      options: {},
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
            label: 'Views',
            data: [65, 59, 80, 81, 56, 55, 40],
            fill: false,
            borderColor: 'rgb(75, 192, 192)',
            lineTension: 0.1
          }
        ]
      }
    };
  }
};
</script>

<style scoped></style>
