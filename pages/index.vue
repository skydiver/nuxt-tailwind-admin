<template>
  <div>
    <MetricCards />
    <Divider />
    <GraphCards />
    <Table />
  </div>
</template>

<script>
import MetricCards from '~/components/_demo/MetricCards.vue';
import GraphCards from '~/components/_demo/GraphCards.vue';
import Table from '~/components/_demo/Table.vue';
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
