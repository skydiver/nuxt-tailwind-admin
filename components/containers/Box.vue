<template>
  <div class="bg-white border rounded shadow">
    <div class="border-b p-3">
      <h5 class="uppercase text-grey-dark">{{ title }}</h5>
    </div>
    <div class="p-5">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Box Title'
    }
  }
};
</script>

<style scoped></style>
