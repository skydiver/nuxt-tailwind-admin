<template>
  <div class="w-full md:w-1/2 p-3">
    <Box title="Graph">
      <LineChart :height="200" :options="options" :chartdata="chartdata" />
    </Box>
  </div>
</template>

<script>
import Box from '~/components/containers/Box.vue';
import LineChart from '~/components/charts/LineChart.vue';

export default {
  components: {
    Box,
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
