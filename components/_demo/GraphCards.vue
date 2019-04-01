<template>
  <div class="flex flex-row flex-wrap flex-grow mt-2">
    <Graph1 />
    <Graph2 />
    <Graph3 />
    <Graph4 />
  </div>
</template>

<script>
import Graph1 from '~/components/_demo/Graph1.vue';
import Graph2 from '~/components/_demo/Graph2.vue';
import Graph3 from '~/components/_demo/Graph3.vue';
import Graph4 from '~/components/_demo/Graph4.vue';

export default {
  components: {
    Graph1,
    Graph2,
    Graph3,
    Graph4
  }
};
</script>
