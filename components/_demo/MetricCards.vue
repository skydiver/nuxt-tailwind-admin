<template>
  <div class="flex flex-wrap">
    <MetricCard
      icon="fa-wallet"
      icon-color="green-600"
      title="Total Revenue"
      value="$3249"
      arrow="up"
      arrow-color="green-500"
    />
    <MetricCard
      icon="fa-users"
      icon-color="orange-600"
      title="Total Users"
      value="249"
      arrow="equal"
      arrow-color="orange-500"
    />
    <MetricCard
      icon="fa-user-plus"
      icon-color="yellow-600"
      title="New Users"
      value="2"
      arrow="up"
      arrow-color="yellow-600"
    />

    <MetricCard
      icon="fa-server"
      icon-color="blue-600"
      title="Server Uptime"
      value="152 days"
    />
    <MetricCard
      icon="fa-tasks"
      icon-color="indigo-600"
      title="To Do List"
      value="7 tasks"
    />
    <MetricCard
      icon="fa-inbox"
      icon-color="red-600"
      title="Issues"
      value="3"
      arrow="up"
      arrow-color="red-500"
    />
  </div>
</template>

<script>
import MetricCard from '~/components/widgets/MetricCard.vue';

export default {
  components: {
    MetricCard
  }
};
</script>

<style scoped></style>
