<template>
  <div>
    <MetricCards />
    <Divider />

    <div class="flex flex-row flex-wrap flex-grow mt-2">
      <div class="w-full md:w-1/2 p-3">
        HELLO
      </div>
    </div>
  </div>
</template>

<script>
import MetricCards from '~/components/Demo/MetricCards.vue';
import Divider from '~/components/Divider.vue';

export default {
  components: {
    MetricCards,
    Divider
  }
};
</script>
