<template>
  <div>
    <Nav />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import Nav from '~/layouts/Nav.vue';
import Footer from '~/layouts/Footer.vue';

export default {
  components: {
    Nav,
    Footer
  },
  head: {
    title: 'Nuxt.js Admin Starter',
    bodyAttrs: {
      class: 'bg-gray-100 font-sans leading-normal tracking-normal'
    }
  }
};
</script>
