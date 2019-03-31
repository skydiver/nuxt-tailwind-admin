<template>
  <div>
    <Nav />
    <nuxt />
  </div>
</template>

<script>
import Nav from '~/components/Nav.vue';

export default {
  components: {
    Nav
  },
  head: {
    bodyAttrs: {
      class: 'bg-grey-lightest font-sans leading-normal tracking-normal'
    }
  }
};
</script>
