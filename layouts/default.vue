<template>
  <div>
    <Nav />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import Nav from '~/components/layout/Nav.vue';
import Footer from '~/components/layout/Footer.vue';

export default {
  components: {
    Nav,
    Footer
  },
  head: {
    title: 'Nuxt.js Admin Starter',
    bodyAttrs: {
      class: 'bg-grey-lightest font-sans leading-normal tracking-normal'
    }
  }
};
</script>
