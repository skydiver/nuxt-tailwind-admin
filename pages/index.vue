<template>
  <div>
    <MetricCards />
    <Divider />
    <GraphCards />
  </div>
</template>

<script>
import MetricCards from '~/components/demo/MetricCards.vue';
import GraphCards from '~/components/demo/GraphCards.vue';
import Divider from '~/components/Divider.vue';

export default {
  components: {
    MetricCards,
    GraphCards,
    Divider
  }
};
</script>
