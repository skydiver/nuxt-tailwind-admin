<template>
  <div class="w-full md:w-1/2 xl:w-1/3 p-3">
    <div class="bg-white border rounded shadow p-2">
      <div class="flex flex-row items-center">
        <div class="flex-shrink pr-4">
          <div :class="bgIconColor" class="rounded p-3">
            <i :class="icon" class="fa fa-2x fa-fw fa-inverse"></i>
          </div>
        </div>
        <div class="flex-1 text-right md:text-center">
          <h5 class="uppercase text-grey">{{ title }}</h5>
          <h3 class="text-3xl">
            {{ value }}
            <span v-if="showArrow" :class="bgArrowColor">
              <i :class="arrowIcon" class="fas"></i
            ></span>
          </h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    icon: {
      type: String,
      default: 'fa-tachometer-alt'
    },
    iconColor: {
      type: String,
      default: 'grey-dark'
    },
    title: {
      type: String,
      default: 'Metric Card'
    },
    value: {
      type: String,
      default: '$0'
    },
    arrow: {
      type: String,
      default: ''
    },
    arrowColor: {
      type: String,
      default: 'grey'
    }
  },

  data() {
    return {
      arrows: {
        up: 'fa-caret-up',
        down: 'fa-caret-down',
        equal: 'fa-exchange-alt'
      }
    };
  },
  computed: {
    bgIconColor() {
      return `bg-${this.iconColor}`;
    },
    showArrow() {
      return this.arrowIcon;
    },
    arrowIcon() {
      return this.arrows[this.arrow] || null;
    },
    bgArrowColor() {
      return `text-${this.arrowColor}`;
    }
  }
};
</script>
