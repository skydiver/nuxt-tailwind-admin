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
          <h5 class="font-bold uppercase text-gray-500">{{ title }}</h5>
          <h3 class="font-bold text-3xl">
            {{ value }}
            <span v-if="showArrow" :class="bgArrowColor"
              ><i :class="arrowIcon" class="fas"></i
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
      required: true
    },
    iconColor: {
      type: String,
      default: 'gray-600'
    },
    title: {
      type: String,
      required: true
    },
    value: {
      type: String,
      default: ''
    },
    arrow: {
      type: String,
      default: ''
    },
    arrowColor: {
      type: String,
      default: 'gray-600'
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
