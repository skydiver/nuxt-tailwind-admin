<template>
  <div class="flex flex-wrap">
    <MetricCard
      icon="fa-wallet"
      icon-color="green-dark"
      title="Total Revenue"
      value="$3249"
      arrow="up"
      arrow-color="green"
    />
    <MetricCard
      icon="fa-users"
      icon-color="orange-dark"
      title="Total Users"
      value="249"
      arrow="equal"
      arrow-color="orange"
    />
    <MetricCard
      icon="fa-user-plus"
      icon-color="yellow-dark"
      title="New Users"
      value="2"
      arrow="up"
      arrow-color="yellow-dark"
    />

    <MetricCard
      icon="fa-server"
      icon-color="blue-dark"
      title="Server Uptime"
      value="152 days"
    />
    <MetricCard
      icon="fa-tasks"
      icon-color="indigo-dark"
      title="To Do List"
      value="7 tasks"
    />
    <MetricCard
      icon="fa-inbox"
      icon-color="red-dark"
      title="Issues"
      value="3"
      arrow="up"
      arrow-color="red"
    />
  </div>
</template>

<script>
import MetricCard from '~/components/MetricCard.vue';

export default {
  components: {
    MetricCard
  }
};
</script>

<style scoped></style>
