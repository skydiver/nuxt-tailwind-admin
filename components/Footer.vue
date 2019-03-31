<template>
  <footer :class="backgroundColor" class="border-t border-grey-light shadow">
    <div class="container max-w-md mx-auto flex py-8">
      <div class="w-full mx-auto flex flex-wrap">
        <div class="flex w-full md:w-1/2 ">
          <div class="px-8">
            <h3 :class="textColor" class="font-bold">
              About
            </h3>
            <p class="py-4 text-grey-dark text-sm">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas
              vel mi ut felis tempus commodo nec id erat. Suspendisse
              consectetur dapibus velit ut lacinia.
            </p>
          </div>
        </div>

        <div class="flex w-full md:w-1/2">
          <div class="px-8">
            <h3 :class="textColor" class="font-bold">Social</h3>
            <ul class="list-reset items-center text-sm pt-3">
              <li>
                <a
                  :class="hoverColor"
                  class="inline-block text-grey-dark no-underline hover:text-underline py-1"
                  href="#"
                  >Add social link</a
                >
              </li>
              <li>
                <a
                  :class="hoverColor"
                  class="inline-block text-grey-dark no-underline hover:text-underline py-1"
                  href="#"
                  >Add social link</a
                >
              </li>
              <li>
                <a
                  :class="hoverColor"
                  class="inline-block text-grey-dark no-underline hover:text-underline py-1"
                  href="#"
                  >Add social link</a
                >
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  computed: {
    darkMode() {
      return this.$store.state.darkMode;
    },
    backgroundColor() {
      return this.darkMode ? 'bg-black' : 'bg-white';
    },
    textColor() {
      return this.darkMode ? 'text-grey-lightest' : 'text-black';
    },
    hoverColor() {
      return this.darkMode ? 'hover:text-grey-lightest' : 'hover:text-black';
    }
  }
};
</script>
