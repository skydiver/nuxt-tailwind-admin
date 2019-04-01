<template>
  <div>
    <MetricCards />
    <Divider />
    <GraphCards />
    <Table />
  </div>
</template>

<script>
import MetricCards from '~/components/demo/MetricCards.vue';
import GraphCards from '~/components/demo/GraphCards.vue';
import Table from '~/components/demo/Table.vue';
import Divider from '~/components/layout/Divider.vue';

export default {
  components: {
    MetricCards,
    GraphCards,
    Table,
    Divider
  }
};
</script>
