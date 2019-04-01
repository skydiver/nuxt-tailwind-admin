<template>
  <BaseContainer>
    <MetricCards />
    <Divider />
    <GraphCards />
    <Table />
  </BaseContainer>
</template>

<script>
import Divider from '~/components/widgets/Divider.vue';
import BaseContainer from '~/components/containers/BaseContainer.vue';
import MetricCards from '~/components/_demo/MetricCards.vue';
import GraphCards from '~/components/_demo/GraphCards.vue';
import Table from '~/components/_demo/Table.vue';

export default {
  components: {
    Divider,
    BaseContainer,
    MetricCards,
    GraphCards,
    Table
  }
};
</script>
