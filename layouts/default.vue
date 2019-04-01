<template>
  <div>
    <Nav />
    <div class="container w-full mx-auto pt-20">
      <div
        class="w-full px-4 md:px-0 md:mt-8 mb-16 text-grey-darkest leading-normal"
      >
        <nuxt />
      </div>
    </div>
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
