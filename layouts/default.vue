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
