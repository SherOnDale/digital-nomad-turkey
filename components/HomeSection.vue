<template>
  <div
    class="home__section"
    :style="{zIndex: index, top: top, transform: `skew(0deg, ${skew}`}"
    :class="{'home__section--bg': !gradient, 'home__section--gradient': gradient}"
  >test</div>
</template>

<script>
export default {
  props: {
    index: Number,
    top: String,
    gradient: {
      type: Boolean,
      default: true
    },
    skew: {
      type: String,
      default: "0deg"
    }
  }
};
</script>

<style>
.home__section {
  position: absolute;
  width: 100%;
  height: 70vh;
  background-color: red;
}

.home__section--bg {
  background-color: var(--accent-one);
}

.home__section--gradient {
  background: linear-gradient(
    to bottom,
    var(--accent-two) 0%,
    var(--accent-two) 10%,
    var(--accent-one) 40%
  );
}
</style>
