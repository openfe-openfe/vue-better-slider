<template>
  <div class="ic-slider-item" :style="style">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'ic-slider-item',
  data() {
    return {
      offset: 0
    };
  },
  computed: {
    style() {
      return {
        width: this.$parent.width + 'px',
        transform: `translate3d(${this.offset}px, 0, 0)`
      };
    }
  },
  beforeCreate() {
    this.$parent.swipes.push(this);
  },
  destroyed() {
    this.$parent.swipes.splice(this.$parent.swipes.indexOf(this), 1);
  }
};
</script>