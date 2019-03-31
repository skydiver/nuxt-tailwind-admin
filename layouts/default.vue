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
import Nav from '~/components/Nav.vue';
import Footer from '~/components/Footer.vue';

export default {
  components: {
    Nav,
    Footer
  },
  computed: {
    darkMode() {
      return this.$store.state.darkMode;
    },
    bodyClass() {
      const defaultClass = 'font-sans leading-normal tracking-normal';
      return this.darkMode
        ? `bg-black-alt ${defaultClass}`
        : `bg-grey-lightest ${defaultClass}`;
    }
  },
  head() {
    return {
      title: 'Nuxt.js Admin Starter',
      bodyAttrs: {
        class: this.bodyClass
      }
    };
  }
};
</script>

<style>
.bg-black-alt {
  background: #191919;
}
.text-black-alt {
  color: #191919;
}
.border-black-alt {
  border-color: #191919;
}
</style>
